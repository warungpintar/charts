## SIERA KUBE WATCH

[siera kube watch](https://github.com/warungpintar/siera-kube-watch) is a Kubernetes events watcher that currently publishes notification to Webhook and Slack. Run it in your k8s cluster, and you will get event notifications.

## TL;DR

```
helm repo add warpincharts  https://warungpintar.github.io/charts
helm search repo warpincharts
helm install siera-kube-watch  -n [your namespace]  warpincharts/siera-kube-watch
or (webhook)
helm install siera-kube-watch -n [your namespace]  warpincharts/siera-kube-watch \
  --set=config.webhook.enabled="true",config.webhook.url="http://webhookurl"
or (slack)
helm install siera-kube-watch -n [your namespace]  warpincharts/siera-kube-watch \
  --set=config.slack.enabled="true",config.webhook.url="http://slackurl"  
or (with value)
helm install siera-kube-watch -n [your namespace] -f values.yaml warpincharts/siera-kube-watch \

```

## Result
![GitHub Logo](example-webhook.png)

## Parameters

The following table lists the configurable parameters of the siera kube watch chart and their default values.

| Parameter                                | Description                                                                                                                 | Default                                                 |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| `metadata.name       `                   | Global name                                                                                                                 | `siera-kube-watch`                                      |
| `image.repository`                       | Image repository                                                                                                            | `warungpintar/siera-kube-watch`                         |
| `image.tag`                              | Image tag                                                                                                                   | `v1.0.0`                                                |
| `image.pullPolicy`                       | Image pull policy                                                                                                           | `IfNotPresent`                                          |
| `config.webhook.enabled`                 | boolean to enable or disable webhook                                                                                        | `false`                                                 |
| `config.webhook.url`                     | url of webhook                                                                                                              | ``                                                      |
| `config.slack.enabled`                   | boolean to enable or disable slack                                                                                          | `false`                                                 |
| `config.slack.url`                       | url of slack                                                                                                                | ``                                                      |


