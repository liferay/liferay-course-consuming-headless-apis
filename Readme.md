# Mastering Consuming Liferay's Headless APIs

This repository contains the Mastering Consuming Liferay's Headless APIs course materials.

## Table of Contents
- [Available Branches](#available-branches)
- [Bundle Preparation](#bundle-preparation)
- [Starting and Stopping the Bundle](#starting-and-stopping-the-bundle)

## Available Branches

There are 2 branches available for the course.
1. **main**: This branch is considered the starting branch for the course and can be used in conjunction with the course content and exercises
2. **final**: This branch is considered the final branch in which the final course content and exercises have been completed

In the **final** branch, all Liferay Client Extensions have been auto-deployed. However, the *clarity-ticketing-action* microservice will need to be started in order to reproduce the Object Client Action exercise.

1. Open a terminal and navigate to the *client-extensions/clarity-ticketing-action/* folder.
2. Start the Spring Boot service (as the microservice is hosted outside of Liferay): 
```
   blade gw bootRun
   ```
3. Reset permissions for the **C_Ticket** object in the **Clarity Ticketing Action OAuth Application User Agent** in the *Control Panel -> OAuth2 Administration* to read/update/delete **C_Ticket data**

## Bundle Preparation

To prepare your local Liferay bundle, you need to use the Blade CLI tool. The Blade CLI provides a convenient way to manage Liferay projects and bundles. Follow the steps below to set up your local environment:

1. **Ensure Blade CLI is Installed**: Make sure you have the Blade CLI installed on your system. If not, you can download it from the [Liferay Blade CLI GitHub page](https://github.com/liferay/liferay-blade-cli).

2. **Navigate to Your Project Directory**: Open a terminal and navigate to the root directory from the cloned repository.

3. **Run the Initialization Command**: Execute the following command to initialize your local Liferay bundle:
   ```
   blade gw initBundle
   ```

   This command will prepare the Liferay bundle and make it available in the `bundles` directory of your project.

4. **Verify the Bundle**: Once the command completes, check the `bundles` directory to ensure that the Liferay bundle has been set up correctly.

By following these steps, you will have a local Liferay bundle ready for development and testing purposes. This setup is essential for running and deploying your Liferay modules effectively.


## Starting and Stopping the Bundle

Once you have prepared your Liferay bundle, you can start and stop it using the Blade CLI tool. Follow the steps below to manage your bundle:

1. **Start the Bundle**: To start your Liferay bundle, execute the following command in your terminal:
   ```
   blade server start
   ```

   This command will start the Liferay server, making it accessible for development and testing.

2. **Access the Environment**: After starting the bundle, open a web browser and navigate to [http://localhost:8080](http://localhost:8080). Use the following credentials to log in:
   - **Username**: admin@clarityvisionsolutions.com
   - **Password**: learn

   This will give you access to the Liferay environment where you can deploy and test your modules.

3. **Stop the Bundle**: When you are done working with the Liferay bundle, you can stop the server by executing the following command:
   ```
   blade server stop
   ```

   This command will stop the Liferay server, freeing up system resources.

By following these steps, you can effectively manage the lifecycle of your Liferay bundle, ensuring a smooth development and testing process.
