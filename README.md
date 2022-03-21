## Github Project Board Creation Automation Hack

_Note: Due to issues with Github Workflow Matrix strategy, this fails intermittently. The other option is to remove the Matrix strategy and map issues and cards manually._

### With these workflow files in your template repo, you create a repo from template, then gh actions will create a project, add columns, create issues, attach issues to board, and cleanup the workflows so they won't run again.

Add the contents of the `/.github` folder to your template repo. 

The `/.github/workflows/project.yeml` needs to be updated on line 6 and `/.github/workflows/cleanup.yaml` on line 10 to match your repo org/name. Commit both of these changes in one commmit. If not, it will run against your template repo.

The `seed-issues` folder contains md files representing the contents of each issue to be created. The `project` workflow creates the project, issues, and assigns issues to board. The `cleanup` workflow deletes the workflow files and project workflow history to prevent someone from inadvertantly running the automation again.

This should be implmented in your own GH organization with a github PAT set as a org secret and then copying from template to a repo in same org. Default name for GH secret is GH_TOKEN,

