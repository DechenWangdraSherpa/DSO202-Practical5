# Prediction (written before rendering)

| Object / field                                   | Base value     | Predicted sandbox value       |
|--------------------------------------------------|----------------|-------------------------------|
| Deployment metadata.name                         | webapp         | sandbox-webapp                |
| Service metadata.name                            | webapp         | sandbox-webapp                |
| ConfigMap metadata.name                          | web-content-<h>| sandbox-web-content-<h>       |
| Deployment volumes[].configMap.name (reference)  | web-content-<h>| sandbox-web-content-<h>       |
| Service spec.selector / Deployment selector      | app: webapp    | UNCHANGED (labels, not names) |
| Container name                                   | nginx          | UNCHANGED (not a resource name)|
| Namespace                                        | (none)         | webapp-sandbox, not prefixed  |
