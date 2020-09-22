### Why we need a Mac

So why do we need a mac instead of the windows laptop.  Well I am hoping that the below bullet points will help you to understand why we need to to our development work on a mac/linux machine.

* We are developing for linux machines using linux code.  By having to use a windows laptop there will always be problems in trying to replicate any errors that we are getting from the linux servers.
* Building docker images on a windows laptop means that they can not be used on a linux host and vic verses.  This means that we are not using the same image on our local windows laptop as we are using in the ci/cd pipeline.
* Development tools like [Terraform](https://www.terraform.io/), [Helm](https://helm.sh/), [Hadolint](https://github.com/hadolint/hadolint) to name a few have been develop for linux/mac machines.  Many of the tools that we use are not available for windows.

We are not trying to do anything new, having the develops/devops on linux/mac's is very normal when youn need to develop and look after linux servers.  Being able to develop with out major code changes due to os changing means that there is a lot more confedence in the code.
