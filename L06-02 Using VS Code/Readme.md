# L06-02

This time, we'll containerize an Express app.  To do that you’ll need to create a Dockerfile.  The Express app files are located in the lab's folder.

## Add a Dockerfile file

Using the Code tooling, add a new Dockerfile by opening the Command Palette from the View menu.

Type **Docker Add** and select **Docker Add Docker Files to Workspace**.

## Build the Docker image

`docker image build --pull --file '/Users/pbalasubramaniam/repos/docker-k8/L06-02 Using VS Code/Dockerfile' --tag 'expressapp:latest' --label 'com.microsoft.created-by=visual-studio-code' '/Users/pbalasubramaniam/repos/docker-k8/L06-02 Using VS Code'`
Open the Command Palette again and issue a **Docker Build**. Code will use the first part of the folder name as the tag. In this case: 04:latest.  Not ideal but you can issue a **Docker Tag** to tag the image with something more useful like express:latest.

## Run an Docker instance

`docker run --rm -d -p 3000:3000/tcp expressapp:latest`
Open the Command Palette again and issue a **Docker Run**.

Point your browser to `http://localhost:3000`

## List the containers running

Click on the Docker icon in the left menu.  You'll be able to see the imahe you just built and the instance that is running.

## Stop the instance

Right click on the instance name and stop it.

## Remove the image

Right click on the image name and delete it.
