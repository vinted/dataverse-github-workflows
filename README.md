# Dataverse github reusable workflows

This repo hosts reusable github workflows defined in `.github/workflows`


## Prerequisites
- Make sure to grant read permission to `dataverse-bot` user to this repo

## Usage

##### Example Caller Workflow

```yaml
  jobs:  
    check-env:
      needs: pr-init
      uses: vinted/dataverse-github-workflows/.github/workflows/dbt-check-env.yml@v1.1.0
      secrets: inherit
```

## TODO
- DBT
    - Extract bash code from `run` sections of actions to bash files
    - Add get images version composite action 
    - Merge test and prod steps
