# Challenge 001: Docker & VPS Deployment

> The steps below are written to work with any VPS provider.

## Overview

Learn to containerize any web application with Docker and deploy it to a live, internet accessible server, complete with a reverse proxy and HTTPS. This challenge walks through the full deployment pipeline, from local development to a secured, production style setup.

## The Challenge Goal

Containerize any web application you've built (or want to build) using Docker, and deploy it successfully to a Virtual Private Server (VPS).

## What You Will Learn

By the end of this challenge, you'll be able to:

- Containerize applications with Docker, including writing a Dockerfile that packages an app and its dependencies.
- Manage a VPS, including remote access and basic Linux server administration.
- Deploy an application from a local machine to a live server.
- Configure a reverse proxy to serve a Dockerized app to the internet.
- Secure a website with a free SSL certificate (HTTPS).

## Milestones

### Milestone 1: Containerize Your Application

- Choose a web application to deploy. It can be a static site, a Node.js backend, a Python Flask app, or anything already running locally.
- Research Dockerfile best practices for your app's language or framework.
- Write a Dockerfile describing how to build your application's image.
- Build the image locally with `docker build`.
- Run and verify the container locally with `docker run`, confirming the app works as expected inside the container.

### Milestone 2: Prepare Your VPS

- Provision a VPS from a hosting provider of your choice.
- Set up SSH access and configure key based authentication instead of password login.
- Perform basic server hardening: update the system, create a non root sudo user, and disable direct root login.
- Configure a firewall (e.g. UFW) to allow only necessary traffic.
- Install Docker Engine on the VPS.

### Milestone 3: Deploy and Run on the VPS

- Transfer your Dockerfile and application code to the VPS (e.g. via `scp` or `git clone`).
- Build the Docker image on the server and run it as a container.
- Configure the container to restart automatically on failure or server reboot.
- Verify the container is running correctly using `docker ps` and `docker logs`.

### Milestone 4: Make It Public and Secure

- Install a reverse proxy (e.g. Nginx or Caddy) on the VPS.
- Configure the reverse proxy to forward incoming traffic on port 80 to your container's mapped port.
- Update the firewall to allow HTTP (80) and HTTPS (443) traffic.
- Optional: point a custom domain at your VPS using a DNS A record.
- Secure the site with a free SSL certificate (e.g. via Let's Encrypt / Certbot).

## What Counts as a Valid Submission

Any project, existing or new, deployed and reachable through your VPS. This can be a static site, a full stack app, a bot with a web dashboard, or anything else with a network facing component.

## Suggested Learning Areas

- Basic Linux server administration
- SSH key based authentication
- Firewall configuration
- Reverse proxies
- Docker container lifecycle and restart policies
- DNS configuration and SSL certificates

## Sharing Your Work

Post your live URL, a short reflection on what you learned, and any issues you ran into in the community. Screenshots of your running container, reverse proxy config, or deployment process are welcome.