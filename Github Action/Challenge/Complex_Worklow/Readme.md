# GitHub Workflow Exercise

This folder contains a simple workflow exercise that demonstrates the use of GitHub Actions. The workflow is triggered by a push event to the repository and consists of four jobs, each running a command to print the current date. Additionally, the choice of the final job depends on the success of the first three jobs.

## Workflow Details

### Trigger
The workflow is triggered by a `push` event to the repository. Whenever you push changes to this repository, the workflow will automatically run.

### Jobs
There are four jobs in this workflow, each with a specific purpose:

1. **Job 1 - Ubuntu Latest Runner**
   - This job runs on an `ubuntu-latest` runner.
   - It prints the current date using a command.

2. **Job 2 - Windows Latest Runner**
   - This job runs on a `windows-latest` runner.
   - It also prints the current date using a command.

3. **Job 3 - macOS Latest Runner**
   - This job runs on a `macos-latest` runner.
   - Like the previous jobs, it prints the current date using a command.

4. **Final Job (Conditional)**
   - The final job is conditional and depends on the success of the first three jobs.
   - If all of the first three jobs (Job 1, Job 2, and Job 3) are successful, this job will be triggered.
   - You have the flexibility to choose the runner and command for this job based on your specific requirements. It will only run if the previous jobs are successful.

## Workflow Configuration

The workflow is defined in a YAML file (`.github/workflows/sample.yml`) within this repository. You can modify the workflow configuration to suit your needs, including changing the runner for the final job and customizing the commands.
