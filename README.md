# Project Name

This project automates the deployment of a Strapi application using CircleCI. The pipeline is configured to pull source code from GitHub, transfer it to a remote server, install dependencies, build the project, and restart the server.

## Prerequisites

- **CircleCI account**: Ensure you have an active CircleCI account connected to your GitHub repository.
- **Remote Server**: A remote server with SSH access to deploy the application.
- **Environment Variables**: Configure the following environment variables in your CircleCI project settings:
  - `user`: SSH user for your remote server.
  - `instance_ip`: IP address of your remote server.

## Pipeline Steps
- **Checkout: Pulls the latest code from the main branch.
- **Create env: Creates an .env file with environment variables.
- **Listing project file: Lists project files and prints the current user.
- **Transfer project files: Transfers project files to the remote server.
- **Install dependencies: Installs project dependencies on the remote server.
- **Build project: Builds the project and restarts the server using PM2.
- **Execute remote commands: Executes additional remote commands for logging.
- **Cleanup: Indicates that the build and deployment process is complete.


## How to Use
- Fork the repository: Fork this GitHub repository to your own account.
- Configure CircleCI: Link your GitHub repository to CircleCI.
- Set environment variables: Set the required environment variables in CircleCI project settings.
- Commit changes: Push your changes to the main branch to trigger the pipeline.