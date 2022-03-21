## Temporary Repo for Testing Github Project Board Creation Automation

The `/.github/workflows/project.yeml` needs to be updated on line 6 to match your repo org/name. If not, it will run against your template repo.

The `seed-issues` folder contains md files representing the cpntents of each issue to be created. The `project` workflow creates the project, issues, and assigns issues to board. The `cleanup` workflow deletes the workflow files and project workflow history to prevent someone from inadvertantly running the automation again.

With these workflow files in your template repo, you create a copy repo, then go to actions and manually start the `project` action. Create new issue md files in seed-isues folder and then update the project workflow file to create and assign them.

This should be implmented in your own GH organization with a github PAT set as a org secret and then copying from template to a repo in same org. Default name for GH secret is GH_TOKEN,
