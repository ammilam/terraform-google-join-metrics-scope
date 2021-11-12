# Join Google Metrics Scope

This module joins a list of GCP projects to a shared metrics scope in [GCP](https://cloud.google.com/).

## Joining A Google Shared Metrics Scope

In order to join one or more projects to a shared metrics scope, declare a module like below... 

```terraform
module "join_metrics_scope" {
  source                 = "ammilam/join-metrics-scope/google"
  version                = "0.1.2"
  metrics_scope_project  = module.monitoring_workspace.project_id # ref to metrics scope created as detailed above
  monitored_projects     = ["project1", "project2"] # enter ref to project(s) needing to be monitored
```