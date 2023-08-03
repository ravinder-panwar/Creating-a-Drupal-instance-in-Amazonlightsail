# Launch a Drupal instance in Amazon Lightsail
 <h3> What is Drupal website?</h3>
 A Drupal website is a website or web application built using the Drupal content management system (CMS). Drupal is an open-source CMS that provides a flexible and powerful framework for creating, managing, and organizing digital content, such as web pages, articles, images, and user accounts.
 
 It may look that a Drupal website is the same as a WordPress website but it is not. <br>
 
**Amazon Lightsail:** Amazon Lightsail is designed to simplify the process of deploying, managing, and scaling applications and websites for developers, small businesses, and other users who may not have extensive cloud expertise

 <h3> Overview steps</h3>
 
**Step 1:** Create a Drupal instance.<br>
**Step 2:** SSH connect to the instance and get the password for your Drupal website.<br>
**Step 3:** Sign in to your Drupal website.<br>
**Step 4:** Create a static IP address and attach it to the instance.<br>
**Step 5:** Create a Lightsail DNS zone.<br>

<h3>Step 1: Create a Drupal instance.</h3>

1. Go to Amazon Lightsail console.
2. On the left navigation pane, click on **Instances**.
3. Click on **Create Instance**.

![1](https://github.com/ravinder-panwar/Launch-a-Drupal-instance-in-Amazon-Lightsail/assets/133412857/4095f1e4-dbc0-4c60-973d-620f530ec549)

4. Select the Region and AV according to your need, choose **Linux** as the platform, and choose **Drupal** as the blueprint.

![2](https://github.com/ravinder-panwar/Launch-a-Drupal-instance-in-Amazon-Lightsail/assets/133412857/8ff710fe-1376-403f-8ca2-de82a4d28eb3)

5. Choose an instance plan.

![3](https://github.com/ravinder-panwar/Launch-a-Drupal-instance-in-Amazon-Lightsail/assets/133412857/6a3e82f6-27fc-4d8a-987e-4edd532783b1)

6. Name your instance as **Drupal-1** and click on **Create Instance.**

![4](https://github.com/ravinder-panwar/Launch-a-Drupal-instance-in-Amazon-Lightsail/assets/133412857/40deacc9-6fa0-4be4-ad9a-bf3c30696136)

<h3>Step 2: SSH connect to the instance and get the password for your Drupal website.</h3>

1. You will now see that your Drupal instance is **running** perfectly.
2. Click on **ssh connect.**

![5](https://github.com/ravinder-panwar/Launch-a-Drupal-instance-in-Amazon-Lightsail/assets/133412857/d4569e48-2a7c-4a88-8aa0-cd9347b9a9c0)

3. After the browser-based SSH client window opens, enter this command to retrieve the default application password: **cat $HOME/bitnami_application_password** and save this password as we will need it in step 3.

![6](https://github.com/ravinder-panwar/Launch-a-Drupal-instance-in-Amazon-Lightsail/assets/133412857/8294e818-be22-4e85-a636-1cc6286ee9ec)

<h3>Step 3: Sign in to your Drupal website.</h3>

1. In a browser, go to http://PublicIpAddress/user/login
**Note:** Paste your Public IP Address.

![now](https://github.com/ravinder-panwar/Launch-a-Drupal-instance-in-Amazon-Lightsail/assets/133412857/9ad5b6fa-4435-490a-818a-e913598911ad)

2. Configure the username as **user** and paste the password that you retrieved in **step 2**.

![7](https://github.com/ravinder-panwar/Launch-a-Drupal-instance-in-Amazon-Lightsail/assets/133412857/a45cf6c4-e566-40b8-9fa3-42dde287971c)

<h3>Step 4: Create a static IP address and attach it to the instance.</h3>

The default public IP for your Drupal instance changes if you stop and start your instance. A static IP address, attached to an instance, stays the same even if you stop and start your instance.

1. Choose your **instance.**
2. Click on **networking.**
3. Click on **Attach static IP.**

![8](https://github.com/ravinder-panwar/Launch-a-Drupal-instance-in-Amazon-Lightsail/assets/133412857/2798fd98-d3c6-4cf4-814c-7efe4eb8df4a)

4. Name the static IP and click on **Create and attach.**

![9](https://github.com/ravinder-panwar/Launch-a-Drupal-instance-in-Amazon-Lightsail/assets/133412857/eb8646ef-b6e4-4c64-9415-3c1a9d01db14)

<h3>Step 5:** Create a Lightsail DNS zone</h3>

1. On the Networking tab, choose **Create DNS zone**.

![10](https://github.com/ravinder-panwar/Launch-a-Drupal-instance-in-Amazon-Lightsail/assets/133412857/7641e70f-dcb4-4ce4-8a49-5284e27f58c0)

2. Enter the Domain name if you have any and click on **Create DNS Zone.**

![11](https://github.com/ravinder-panwar/Launch-a-Drupal-instance-in-Amazon-Lightsail/assets/133412857/88016476-98fb-4f29-bbe2-bc84b9c80f1e)

3. Add an **A record** to point the apex of your domain to your Drupal instance.

4. In the Maps to box, choose the static IP that you attached to the Drupal instance.

![12](https://github.com/ravinder-panwar/Launch-a-Drupal-instance-in-Amazon-Lightsail/assets/133412857/cccc0966-7e83-49bf-beed-6bc3d55a4bae)

<h2> Congratulations! Project Completed.</h2>








































