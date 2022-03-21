## Temporary Repo for Testing Github Porject Board Creation Automation

Due to challenges with Github action triggers with create repo from template, the base trigger is manual.

The `seed-issues` folder contains md files representing the cpntents of each issue to be created. The `project` workflow creates the project, issues, and assigns issues to board. The `cleanup` workflow deletes the workflow files and project workflow history to prevent someone from inadvertantly running the automation again.

With these workflow files in your template repo, you create a copy repo, then go to actions and manually start the `project` action. Create new issue md files in seed-isues folder and then update the project workflow file to create and assign them.
