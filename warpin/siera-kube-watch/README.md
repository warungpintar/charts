## SIERA KUBE WATCH

[siera kubewatch](https://github.com/warungpintar/siera-kube-watch) is a Kubernetes events watcher that aims to publish incident (unexpected event) as a notification through webhooks.

Supported webhooks:
- slack
- workplace chat
- webhook

## TL;DR

add repository 
```
helm repo add warpincharts  https://warungpintar.github.io/charts
helm search repo warpincharts
```

install with webhook
```
helm install siera-kube-watch -n [your namespace]  warpincharts/siera-kube-watch \
  --set=config.webhook.enabled="true",config.webhook.url="http://webhookurl"
```
install with slack
```
helm install siera-kube-watch -n [your namespace]  warpincharts/siera-kube-watch \
  --set=config.slack.enabled="true",config.webhook.url="http://slackurl" 
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


Alternatively, a YAML file that specifies the values for the above parameters can be provided while installing the chart. For example,
 
```
helm install siera-kube-watch -n [your namespace] -f values.yaml warpincharts/siera-kube-watch 
```
