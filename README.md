## Github Project Board Creation Automation Hack

With these workflow files in your template repo, you create a repo from template, then gh actions will create a project, add columns, create issues, attach issues to board, and cleanup the workflows so they won't run again.

Add the contents of the `/.github` folder to your template repo. 

The `/.github/workflows/project.yeml` and `/.github/workflows/cleanup.yaml` on `if:` lines to match your org/repo. Commit both of these changes in one commmit. If not, it will run against your template repo.

The `seed-issues` folder contains md files representing the contents of each issue to be created. The `project` workflow creates the project, issues, and assigns issues to board. The `cleanup` workflow deletes the workflow files and project workflow history to prevent someone from inadvertantly running the automation again.

