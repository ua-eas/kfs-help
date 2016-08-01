University of Arizona kfs-help
===

This project contains the help text that is integrated with the UAccess Financials application.

Background
------

This project is forked from the kuali/kfs-help repository (https://github.com/kuali/kfs-help). The version of that code is 5.4.0, and the artifact resides at http://nexus.kuali.org/content/groups/public/org/kuali/kfs/kfs-help/5.4.0/kfs-help-5.4.0.jar.

We changed the versioning to follow the convention that we established for the KFS and Rice code:

**_snapshot name:_** ua-releaseX-SNAPSHOT
**_release name:_** ua-releaseX

*X* represents an integer.

Branch Info
------

The current branches in this project and their intended destination are as follows:

| Branch           | Purpose      |
| ---------------- |:-------------|
| ua-development   | development and testing environments that are running our daily snapshot build |
| ua-master        | QA, support, and production environments that are running our release build |
| feature branches | temporary branches used for development, which are archived after they are included in a release |
| master           | original master branch of forked repository |

Usage
------

Currently requires Maven 3.0 or greater.

Building this project will result in a kfs-help-ua-releaseX or kfs-help-ua-releaseX-SNAPSHOT jar file.

An example command you can use to build this and install it to your local Maven repository is: 

```sh
mvn clean install
```

This is helpful for local testing.

For our overall project use, we will build and deploy the jar to our local Nexus repository. This means the .jar files will be in one of these two locations:

| Type      | Location |
| --------- | :------- |
| snapshots | https://ka-tools.mosaic.arizona.edu/nexus/service/local/repositories/snapshots/content/org/kuali/kfs/kfs-help/ |
| releases  | https://ka-tools.mosaic.arizona.edu/nexus/service/local/repositories/releases/content/org/kuali/kfs/kfs-help/ |

Making Changes
------

Developers who would like to make changes to the help text should do the following:

1. Follow our source code control process as outlined on Confluence here: https://confluence.arizona.edu/display/KATT/Source+Control+Management+with+GitHub+Work+Instructions
2. Make sure to inform DevOps of a kfs-help change, so the kfs.help.version in the KFS project can be updated accordingly.
