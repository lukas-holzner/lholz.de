---
title: "Getting started with Authentik"
categories:
  - Docker
tags:
  - traefik
  - ansible
  - auth
---

For a while now, i was thinking about centralizing user authentication for my hosted services. Features, i was searching for were:
- Basic Authetication with forewardAuth/Oauth/etc.
- Webfrontend for user management (not just an ldap command line)
- User Groups
- Self hosted

I had a look at Authelia before. Unfortunatly Authelia only has Authentication providers for files and ldap. Which are both don't provide a Webfrontend for usermanagement out of the box. There are forontends for ldap, but they are not built in and a hassle to set up.

A friend mentioned Authentik, so I had a look at it.

# Infrastructure

The setup I have is the following:

- Virtual Server in the Cloud:
  - Traefik as a reverse proxy for my Services
  - Docker for hosting all my containers
  - Services like: Gitea, Paperlessngx, Nextcloud, codeserver .. in containers

I wanted to integrate authentik into this infrasturcture, by using the proxy provider from authentik and having it provide authentication with a traefik forward auth middleware.

