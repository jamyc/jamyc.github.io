---
title:  "Bridge to Kubernetes"
date:   2020-10-09 14:55:14 +0200
categories: posts
excerpt: "A figurative bridge between your development workstation and your Kubernetes cluster."
---

# What is it?
Previously known as 'Local Process with Kubernetes', Microsoft recently [announced](https://devblogs.microsoft.com/visualstudio/bridge-to-kubernetes-ga/) General Availability of 'Bridge to Kubernetes' (I like the name change!). Bridge to Kubernetes is a tool that allows you to easily write, test and debug microservice code on your development workstation, while still being connected with other services in your Kubernetes cluster. 

> Bridge to Kubernetes is an iterative development tool offered in Visual Studio and VS Code that allows developers to write, test and debug microservice code on their development workstations while consuming dependencies and inheriting existing configuration from a Kubernetes environment. 

Simply put, we can run one of our services on our development workstation and with the help of Bridge to Kubernetes, the cluster traffic to that specific service will be redirected to our development workstation.

# Prerequisites
- Install the Bridge to Kubernetes [VS Code extension](https://aka.ms/bridge-to-k8s-vsc-extension)

If you are using Visual Studio, you can find the extension [here](https://aka.ms/bridge-to-k8s-vs-extension), however this post only covers the VS Code steps.
{: .notice--info}

This is some text about prereqs.

- Note: Not suggested to run this in production (link?).

# Getting started in VS Code
I already have a few services running in Azure Kubernetes Service and have configured the Kubernetes CLI to be connected to my cluster using:
```bash
az aks get-credentials \
  --resource-group MyResourceGroup \
  --name MyAKS
```

Set your default namespace:
```bash
kubectl config set-context --current --namespace=mynamespace
```



# Isolation mode
This is some text about isolation mode.

## Header propagation
For this to work, you need to propagate the headers.

# Limitations / Issues
- WSL, doesn't quite work yet
- Service can only have 1 pod for this to work, should be fine in development

# Moving forward



def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')
#=> prints 'Hi, Tom' to STDOUT.


## Yas
Check out the [Jekyll docs][jekyll-docs] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll Talk][jekyll-talk].

[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/
