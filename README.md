# Action Markdown
-----------------

GitHub Action to expose parameters specified in the `action.yaml` metadata file.

## Usage

```yaml
- name: action-markdown
  id: action-md
  uses: Shresht7/action-markdown@main
  with:
    path: ./action.yml # Path to the action metadata file (default: ./action.yaml)

- name: some-other-action
  uses: user/some-other-action@v1
  with:
    description: ${{ steps.action-md.outputs.description }}
    inputs: ${{ steps.action-md.outputs.inputs-md-table }}
```

## Inputs

<!-- slot: inputs -->


| input | description | default |
| ----- | ----------- | ------- |
| path | Path to the `action.yaml` metadata file | **required** |
| prettyPrint | Beautify markdown table | `false` |


<!-- /slot -->

## Outputs

<!-- slot: outputs -->


| outputs | description |
| ------- | ----------- |
| inputs-md-table | Markdown table of the action inputs |
| outputs-md-table | Markdown table of the action outputs |


<!-- /slot -->