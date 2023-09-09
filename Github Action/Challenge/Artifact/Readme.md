# Workflow Requirements

This document outlines the requirements for configuring a workflow in your repository.

## Trigger

- The workflow must be triggered by a **push event**.

## Environment Variable

- At the start of the workflow, create an environment variable named **"ARTIFACT_NAME"** to store the name of the artifact.

## Workflow Structure

- The workflow must include a single job with **two steps**.
- **Step 1**: Utilize the **checkout action** to check out all code from the repository.
- **Step 2**: Use the **upload artifact action** to create an artifact. The artifact's name should be determined dynamically based on the **"ARTIFACT_NAME"** environment variable.

By following these requirements, your workflow will be triggered by a push event, use an environment variable for artifact naming, and consist of two specific steps.
