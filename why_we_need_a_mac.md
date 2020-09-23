### Why we need a Mac

So why do we need a mac instead of the windows laptop.  Well I am hoping that the below bullet points will help you to understand why we need to to our development work on a mac/linux machine.

* We are developing for linux machines using linux code.  By having to use a windows laptop there will always be problems in trying to replicate any errors that we are getting from the linux servers.
* Building docker images on a windows laptop means that they can not be used on a linux host and vic verses.  This means that we are not using the same image on our local windows laptop as we are using in the ci/cd pipeline.
* Development tools like [Terraform](https://www.terraform.io/), [Helm](https://helm.sh/), [Hadolint](https://github.com/hadolint/hadolint) to name a few have been develop for linux/mac machines.  Many of the tools that we use are not available for windows.

We are not trying to do anything new in the world outside the bank, having the develops/devops on linux/mac's is very normal when you need to develop and look after linux servers.  Being able to develop with out major code changes due to os changing means that there is a lot more confedence in the code.

Having develops/devops using mac's/linux machines has been standard pratice for many years in the industry.  So this is only something new for the bank to do not something new for the indusrty.

Using mac laptop's is the prefered way of doing this but in total we belive that there are five ways of doing things.  Below are the five ways with pros and cons.

Name | Pro | Con |
---- | --- | --- |
Mac | No code changes needed as unix based os.  The same code and pipelines that are being used in the bank can be run directly for easy of development. | Extra expense |
Build server | No code changes needed as unix based os.  The same code and pipelines that are being used in the bank can be run directly for easy of development. | Build server is shared so to make sure your code does not interfere with each other you would need to run your own docker/vm on the build server.  With multiple people using the same build server it would be come very slow at times as it would be under heavy load. Any problem with internet and you will not be able to work. |
cygwin | A semi full linux running directly on windows.  Would be at least better than git bash. | Would still need two docker images as still testing on a windows os.  Some software would still not work on this as it is still windows os. Would still not be able to have docker and Virtualbox running at same time. |
Full linux VM | No code changes needed as unix based os.  The same code and pipelines that are being used in the bank can be run directly for easy of development.| Would be slow as it would be shareing hardware with windows.  Likly to be a problem in getting virtualbox and docker running at same time. |
BYOD Linux | Only need VPN details to get up and running.  Would allow for very quick POC work. | |
