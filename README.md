**Tar File Creation Workflow**

**Follow these steps to create a tar file:**

1. Navigate to .github/workflows/main.yaml and update the versions as per your requirements. Commit the changes.
2. Run the action to build the tar of the images. Proceed to the Actions tab and select Docker Image Pull and Tar Creation. Click on Run Workflow.
3. Once the job is successfully completed, go to the summary section and scroll down to the bottom. You can download the artifact containing all the images in a tar file.
4. To load these images into Docker, execute the following command:
`docker load -i docker-images.tar`
5. If you wish to load images into the containerd registry, use the following command:
`sudo ctr images import /path/of/docker-images.tar containerd://*;`
