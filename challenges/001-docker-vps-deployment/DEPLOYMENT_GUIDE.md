Welcome to the Deployment Journey!
================================

Welcome to the Dockerize & Deploy Any Website challenge!

Submission Deadline: You Have 2 Weeks!
-------------------------------------------------
You have until 12 July 2025 01:00 to work on your project and submit your final deployment. We encourage you to start early, utilize the provided resources, and ask questions in the support channel (archived-vps-docker-challenge or your project's support channel).

Over the next two weeks, you'll transform your web application from local code to a live, internet-accessible site. This challenge is designed to build your skills in two powerful areas: Docker for consistent environments and a VPS for full control over your hosting.

Your First Mission: Prepare Your Foundation!
--------------------------------------------

Choose Your Weapon: Decide which web application you'll be deploying. It can be a simple static HTML site, a Node.js backend, a Python Flask app, or anything you've built, just ensure it is running smoothly on your local machine.

Understand Containerization: Begin by researching "What is Docker?" and "Why use Docker?". Think about the problem Docker solves.

Stuck? Ask for help in the project's support channels.

Milestone 1: Your App in a Box!
--------------------------------

Great job setting the stage! Now it's time to put your application into its very own isolated environment.

Containerize Your Application!

- Craft Your Blueprint: Research "Dockerfile best practices" for your application's language/framework (e.g., "Node.js (Express) Dockerfile", "Python Flask Dockerfile", "React or Vue site Dockerfile"). Your goal is to create a Dockerfile that tells Docker exactly how to build your application's image.
- Build Your Image: Learn how to use `docker build` to transform your Dockerfile into a portable Docker image on your local machine.
- Test Your Box: Use `docker run` to start your container and verify that your application is running correctly inside its container, accessible on a local port.

Remember: Docker images are like packages, and containers are running instances of those packages. This step ensures your package is perfect before shipping!

Milestone 2: Accessing Your Remote Playground
--------------------------------------------

Your app is now neatly packaged in a Docker image locally! Before we send it off, let's get your VPS ready to receive it.

Secure Your VPS & Install Docker!

1. Get Your Virtual Server: If you haven't already, provision a VPS. This will be your playground for deployment.
2. Connect Securely: Research "SSH access to VPS" and "SSH key authentication". Learn how to log into your VPS using your terminal and set up password-less, key-based authentication for enhanced security.
3. Initial Server Hygiene: Implement basic security steps (updates, create a non-root sudo user, disable direct root login). Research "Ubuntu server initial setup" if you're using an Ubuntu image.
4. Firewall First Line of Defense: Research "UFW firewall setup Ubuntu". Configure a basic firewall to only allow essential traffic (like SSH and, later, web traffic) to your server.
5. Bring Docker Aboard: Research "install Docker on Ubuntu 24.04 LTS" (or your chosen distro). Install Docker Engine on your VPS.

Pro Tip: Every command you run on your VPS affects the live server. Double check before you hit Enter.

Milestone 3: Your App, Live on the Server!
-----------------------------------------

You've got your app containerized and your VPS ready. It's deployment time!

Deploy & Run on VPS!

- Code Transfer: Choose how you will get your Dockerfile and application code to the VPS, for example `scp`, `rsync`, or `git clone`.
- Build & Run Remotely: On the VPS, use `docker build` to create the image and `docker run` to start your application in a Docker container.
- Keep it Running: Ensure your Docker container runs continuously, even after server reboots. Research Docker restart policies (e.g., `--restart unless-stopped`).
- Verify Internally: Use `docker ps` and `docker logs` to confirm the container is running and healthy.

Critical Thinking: Your application might be running on an internal port (e.g., 3000). Map that to a port on the VPS so your reverse proxy can access it.

Milestone 4: Making Your Website Public & Secure!
------------------------------------------------

Your app is alive on the VPS, but how do people access it? And how do we make it secure?

Nginx & SSL! The Web Gateway:

1. Nginx as a Reverse Proxy: Research "Nginx as a reverse proxy for Docker". Install Nginx on your VPS.
2. Configure Routing: Create an Nginx configuration that listens on port 80 (HTTP) and forwards requests to the port your Docker container is mapped to (e.g., `localhost:8080`).
3. Open the Gates: Update your UFW firewall to allow HTTP (port 80) and HTTPS (port 443) traffic.
4. Connect Your Domain (Optional but Recommended): If you have a custom domain, add an A record pointing to your VPS IP address.
5. Secure with HTTPS: Research "Let's Encrypt Certbot Nginx". Install Certbot and use it to obtain and configure a free SSL certificate for your domain to enable HTTPS.

Final Check: Visit your domain (or VPS IP if you don't have a domain) in your browser. Does your website load? Is it secure (HTTPS)?

Final Call: Submission Time!
---------------------------

Final Reminder! This challenge is about Dockerizing and deploying any website to a VPS in 2 weeks. The final submission deadline is 12 July 2025 01:00.

Your Final Mission: Submit Your Proof of Learning!

Ensure you've covered all the requirements:

- Your live website URL.
- Screenshots demonstrating your Docker container's health, Nginx config, and successful deployment.
- Your project code repository link (with Dockerfile).
- Your personal reflection on what you learned and how you overcame challenges.

Submission link and support channels: Use the challenge's submission form and support channel to submit and ask for help.

Project Sharing & Help Session
-----------------------------

If you feel stuck, or want to share progress, join the community help session (check the challenge channels for dates and links).

Additional resources:

- Intro video on deploying with Docker and a VPS: https://www.youtube.com/watch?v=U8De7gavikI

Good luck, we can't wait to see your deployed projects!
