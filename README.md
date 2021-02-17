# Task 2: Packaging a Buildpack

Welcome to the Paketo Buildpacks tutorial.

This repository consists of a set of branches,
Each branch has a particular task designed to familiarize
you with the Paketo Buildpacks project.

Each subsequent task gets progressively more technical,
so feel free to dive as deep as you would like.

Index:
-
- Task 0: Introduction & The Application Image
- Task 1: Paketo Artifacts Overview
- Task 2: **Packaging a Buildpack**
- Task 3: Packaging a Metabuildpack
- Task 4: Create a custom Metabuildpack
- Task 5: Creating a Builder
- Task 6: Rolling Your Own Implementation Buildpack
- Task 7: The Packit Library

## Prerequisites

For this task you will need a couple additional pieces of software
 - [pack](https://buildpacks.io/docs/install-pack/)
   - This is the CLI that orchestrates the running of each Paketo buildpack
 - [docker](https://docs.docker.com/get-docker/)
   - Provides an image registry on all platforms.
 - [sample_application](https://github.com/dwillist/onboarding_application)
   - just a simple application nodejs application we are going to build
   -    This app will be used throughout this tutorial so it is recommended that you use it
- [git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
- [paketo-buildpacks/node-engine repository](https://github.com/paketo-buildpacks/node-engine)
    - this can be clone by running
    ```git clone https://github.com/paketo-buildpacks/node-engine```
- [paketo-buildpacks/node-start repository](https://github.com/paketo-buildpacks/node-start)
    - this can be clone by running
    ```git clone https://github.com/paketo-buildpacks/node-start```

## Packaging a Buildpack

Ok, this is the first task where we will ask you the reader to complete a task, with a few hints (hopefully helpful)

## Packaging a Buildpack

For this task we would like you to do the following,
 1) package the `node-engine` and `node-start` buildpacks from source into both `buildpackages` and `buildpacks` (should be a single command)

 2) run a successful `pack build` of the `sample_application` using the `node-engine` and `node-start` **buildpack archives** that you packaged in step 1.

 3) run a successful `pack build` of the `sample_application` using the `node-engine` and `node-start` **buildpackage images** that you packaged in step 1.

Hints:
-
- there is a script in both the `node-engine` and `node-start` repos called `package.sh`, you should probably use this
- Recall order of buildpacks matter when running `pack build`

Extra:
-
- Try and use [`skopeo`](https://github.com/containers/skopeo) to import the `buildpackage.cnb` artifacts into your local docker registry. Then build using these.



