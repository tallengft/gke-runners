# gke-runners

Using guide found [here](https://github.blog/2020-08-04-github-actions-self-hosted-runners-on-google-cloud/)

# Into
GitHub Actions help you automate your software development workflows. You’re probably already familiar with the built-in runners for Windows, Linux, and macOS, but what if your workloads require custom hardware, a specific operating system, or software tools that aren’t available on these runners?

[Self-hosted runners](https://docs.github.com/en/free-pro-team@latest/actions/hosting-your-own-runners/about-self-hosted-runners) give you freedom, flexibility, and complete control over your GitHub Actions execution environment. These runners can be physical servers, virtual machines, or container images, and they can run on-premises, on a public cloud like [Google Cloud](https://cloud.google.com/), or on both using a platform like [Anthos](https://cloud.google.com/anthos). Here are some use cases for GitHub Actions self-hosted runners:

Run with more memory and CPU resources for faster build and test times.
Leverage access to custom hardware like GPUs and TPUs.
Choose different processor architectures like ARM.
Interact with the physical world using ROS and serial-attached robots.
Access information only available within your organization’s security perimeter like credentials or certificates.
Integrate with “behind the firewall” resources and other non-external systems.
This post explores patterns for configuring and maintaining GitHub Actions self-hosted runners on Google Cloud.

# Persistent runners on Kubernetes Engine
