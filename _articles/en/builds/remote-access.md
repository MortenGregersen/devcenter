---
changelog: 'New tutorial video has been published about setting up and using remote
  access to help you debug your builds. '
last_modified_at: 2020-05-06T14:00:00.000+00:00
title: Remote access
redirect_from: []
tag:
- builds
- troubleshooting
description: Access our build machines remotely when running a failed build again.
  You can use either SSH or a screenshare app to log in to the build's virtual machine.
new_article: false
summary: ''
menu:
  builds-main:
    weight: 33

---
{% include video.html embed_url="https://www.youtube.com/embed/PbKDilX1gB4" %}

Remote access allows users to connect to their build's virtual machines via SSH or a screenshare app. A failed build can be rebuilt with remote access enabled to make troubleshooting a lot easier - for example, if the build logs don't provide enough information about the error.

{% include message_box.html type="important" title="Authorization" content="Users who have the **Testers/QA** roles on the app CANNOT use remote access."%}

There are two ways to use remote access on our build machines:

* **SSH**: this is available for both Linux/Docker based and MacOS machines.
* **Screenshare**: this is only available for MacOS machines. It uses the VNC system.

With either method, you can access the build machine remotely during the build and for 10 minutes after the build is finished.

## Remote access with SSH

1. Go to the build page.
2. Click the **Rebuild with Remote Access** option.
3. Click **Remote Access Instructions**.

   ![](/img/remote-access-instructions.png)
4. Under the **SSH** option, find and copy the command you will need.
5. Open a command line interface.
6. Run the command found under **SSH** (the below is an example):

       ssh -o StrictHostKeyChecking=no vagrant@1.tcp.ngrok.io -p 000000
7. Copy and paste the password from the **Remote Access Instructions** page.

And done! You should be able to access the virtual machine where your build is running.

## Remote access with screenshare

1. Go to the build page.
2. Click the **Rebuild with Remote Access** option.
3. Click **Remote Access Instructions**.

   ![](/img/remote-access-instructions.png)
4. Under the **Screenshare** option, find the required information:
   * Address
   * Username
   * Password
5. Open a VNC screenshare application.

   The simplest option is using the default **Screen Sharing** application on macOS.
6. Fill out the required fields with the information from under the **Screenshare** option.

And done! You should now be able to access the virtual machine where your build is running.

{% include banner.html banner_text="Connect to a VM with Remote Access" url="https://app.bitrise.io/users/sign_up?utm_source=devcenter&utm_medium=bottom_cta" button_text="Go to your app" %}