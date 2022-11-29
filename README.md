### Unfortunately, the changes Github made to projects broke this - no longer works

## Hack to Create Github Project Board with Issues Addded on Create Repo from Template

With these workflow files in your template repo, you create a repo from template, then gh actions will create a project, add columns, create issues, attach issues to board, and cleanup the workflows so they won't run again.

The cleanup workflow file is set to manual execution by default. Beware that it will delete all workflow history from your repo.

Add the contents of the `/.github` folder to your template repo. Edit the `/.github/workflows/project.yeml` and `/.github/workflows/cleanup.yaml` on appropriate `if:` lines to match your org/repo. Commit both of these changes in one commmit. If not, it will run against your template repo.

The `seed-issues` folder contains md files representing the contents of each issue to be created, issues will be added to the board matching their order in the file system. The Github matrix strategy is set to max of five concurrent jobs to preven interfering with other organizational job requirements.

