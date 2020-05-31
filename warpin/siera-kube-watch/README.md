#SIERA KUBE WATCH

siera kube watch is a Kubernetes events watcher that currently publishes notification to Webhook and Slack. Run it in your k8s cluster, and you will get event notifications.


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


