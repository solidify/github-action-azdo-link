# Add Azure DevOps Work Item link to Pull Request
This GitHub action will create a link to a work item in Azure DevOps in a new Pull Request comment if you added a reference, ex. AB#123,  in your Pull Request's title or description, where the number is a work item id from Azure DevOps.

## Usage

### Inputs
- `organization`: Azure DevOps Organization
- `projectName`: Azure DevOps Team Project
- `GITHUB_TOKEN`:  ${{secrets.GITHUB_TOKEN}}


## Example usage
### Add a trigger on Pull Request
```yaml
on:
  pull_request:
    branches: [ master ]
```
### Add a step 
```yaml
- name: Get azdo wi link step
        uses: solidify/github-action-azdo-link
        with:
          organization: 'Org Name'
          projectName: 'Team Project Name'
          GITHUB_TOKEN: ${{secrets.GITHUB_TOKEN}}
``` 

## License
The scripts and documentation in this project are released under the [MIT License](LICENSE)
