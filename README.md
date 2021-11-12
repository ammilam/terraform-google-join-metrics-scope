# Join Metrics Scope Module

This module joins a list of GCP projects to a shared metrics scope in [GCP](https://cloud.google.com/).

## Joining A Program's Shared Metrics Scope

In order to join a project to a shared metrics scope, declare a module like below... The module accepts a list of projects in case more than one need to be added from a repo.

```terraform
module "join_metrics_scope" {
  source                 = ""
  metrics_scope_project  = module.monitoring_workspace.project_id # ref to metrics scope created as detailed above
  monitored_projects     = [""] # enter ref to project(s) needing to be monitored
```
