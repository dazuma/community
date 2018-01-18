---
title: Using Alpine Linux with Ruby on Google Cloud Platform
description: Learn the tricks and techniques for getting Ruby applications to run effectively on Google Cloud using Alpine Linux
author: dazuma
tags: Alpine Linux, Ruby, Rails, Docker, Kubernetes
date_published: 2018-01-31
---

The [Alpine Linux](https://alpinelinux.org/) distribution has increasingly
become a popular platform for deploying server-side applications, due to its
low overhead and security focus. However, because of some of Alpine's
architectural choices, a few small changes may be necessary to get Ruby
applications running effectively on Google Cloud Platform using Alpine.

This tutorial teaches you some basic techniques for using Alpine Linux for your
Ruby application on Google Cloud. It walks you through writing a simple
translation website and deploying it to Google Cloud. Along the way, you will
complete the following objectives:

*   Create a Docker image of a Ruby application on Alpine Linux
*   Access Google Cloud APIs from Alpine Linux
*   Learn techniques to minimize the image size
*   Deploy your Docker image to Kubernetes or Google App Engine

## Before you begin

Before running this tutorial, you will need to install Docker. Find the
appropriate download link for your operating system on the
[Docker website](https://www.docker.com/community-edition).

Additionally, take the following steps to set up your Google Cloud Platform
(GCP) project and tools:

1.  [Create a new GCP project](https://console.cloud.google.com/projectcreate).
    Remember the name of your project (generally three words or numbers separated
    by hyphens). We refer to the project as `[PROJECT-ID]` throughout this tutorial.
    When you create a project, GCP automatically enables the Cloud SQL API.

1.  [Enable billing](https://cloud.google.com/billing/docs/how-to/modify-project#enable_billing_for_a_project)
    for your project.

1.  Install the [Google Cloud SDK](https://cloud.google.com/sdk/). The Cloud SDK
    contains the `gcloud` command-line tool, which is the primary tool for
    interacting with GCP.

1.  [Initialize the `gcloud` command-line tool](https://cloud.google.com/sdk/docs/initializing)
    by running `gcloud init` from your shell or terminal. Set the default
    project to the project you created. Configure Google Compute Engine to set
    the default _compute zone_ to a zone in your nearest geographical region,
    such as `us-central1-a`. We refer to the compute zone as `[COMPUTE-ZONE]`
    throughout this tutorial.

## Creating an Alpine-based Docker image for your Ruby app

The low overhead of Alpine makes it an ideal base operating system for Docker
images. In this section, you learn how to construct an Alpine-based Docker
image for your Ruby application, suitable for deployment to a Docker-based
hosting environment such as Google Kubernetes Engine or Google App Engine.

### Create a new Rails application



### Dockerize the Rails app using the Ruby-Alpine base image



## Accessing Google Cloud APIs from Alpine Linux



### Add a translate feature



### Adjust the Gemfile for Alpine compatibility



## Precompiling assets in an Alpine-based Docker image



## Deploying an Alpine-based image to GCP



### Deploying to Google App Engine



### Deploying to Google Kubernetes Engine



## Next steps

