# k8s-ci-build

A Node.js application with a fully automated CI/CD pipeline that builds, containerizes, and deploys to Kubernetes using GitHub Actions.

## Overview

This project demonstrates an end-to-end CI/CD workflow for a JavaScript application. The pipeline automatically builds a Docker image on every push and deploys it to a Kubernetes cluster, ensuring fast and reliable delivery.

## Project Structure


├── .github/workflows/   # GitHub Actions CI/CD pipeline configuration
├── src/                 # Application source code (Node.js)
├── Dockerfile           # Docker image build configuration
└── README.md            # Project documentation


## Tech Stack

•⁠  ⁠*Runtime:* Node.js
•⁠  ⁠*Containerization:* Docker
•⁠  ⁠*CI/CD:* GitHub Actions
•⁠  ⁠*Orchestration:* Kubernetes

## Prerequisites

Before running this project locally, make sure you have the following installed:

•⁠  ⁠[Node.js](https://nodejs.org/) (v16 or higher)
•⁠  ⁠[Docker](https://www.docker.com/)
•⁠  ⁠[kubectl](https://kubernetes.io/docs/tasks/tools/) — configured and connected to your cluster

## Getting Started

1.⁠ ⁠Clone the repository:

⁠ bash
git clone https://github.com/jwebsite-go/k8s-ci-build.git
cd k8s-ci-build
 ⁠

1.⁠ ⁠Install dependencies:

⁠ bash
npm install
 ⁠

1.⁠ ⁠Run locally:

⁠ bash
npm start
 ⁠

## Docker

Build the image manually:

⁠ bash
docker build -t k8s-ci-build .
docker run -p 3000:3000 k8s-ci-build
 ⁠

## CI/CD Pipeline

The GitHub Actions workflow (located in ⁠ .github/workflows/ ⁠) automates the following steps on every push to the main branch:

1.⁠ ⁠Installs dependencies and runs tests
1.⁠ ⁠Builds a Docker image
1.⁠ ⁠Pushes the image to the container registry
1.⁠ ⁠Deploys the updated image to the Kubernetes cluster

