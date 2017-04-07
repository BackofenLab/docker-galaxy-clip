[![Build Status](https://travis-ci.org/BackofenLab/docker-galaxy-clip.svg?branch=master)](https://travis-ci.org/BackofenLab/docker-galaxy-clip)
[![Docker Repository on Quay](https://quay.io/repository/bgruening/galaxy-clip/status "Docker Repository on Quay")](https://quay.io/repository/bgruening/galaxy-clip)

Galaxy-CLIP
========================
Galaxy-CLIP is a web-based environment for the analysis of different kinds of CLIP data. It consists of a set of integrated Galaxy tools and different workflows for the analysis of CLIP data.

:whale: Galaxy-CLIP-Docker Image
========================
This Docker image is a flavor of [Galaxy Docker image](https://github.com/bgruening/docker-galaxy-stable) customized by integrating different CLIP tools and workflows.

Table of Contents
=================
 
   * [Installation and Setup:](#installation-and-setup)
      * [Requirements:](#requirements)
      * [Running the Galaxy server](#running-the-galaxy-server)
         * [From the command line (Linux/Windows/MacOS):](#from-the-command-line-linuxwindowsmacos)
         * [Using Kitematic graphic interface (Windows/MacOS):](#using-kitematic-graphic-interface-windowsmacos)
   * [Usage - How to run Galaxy-GraphClust:](#usage---how-to-run-galaxy-clip)
      * [Browser access to the server:](#browser-access-to-the-server)
      * [Registration and Login:](#registration-and-login)
      * [Help](#help)
         * [Interactive tours](#interactive-tours)
   * [CLIP pipeline overview](#clip-pipeline-overview)
   * [Contributors](#contributors)
   * [Support &amp; Bug Reports](#support--bug-reports)



# Installation and Setup:
## Requirements:

The only requirement to run this webserver locally is [Docker](https://docs.docker.com/installation).
Docker supports the three major desktop operating systems  Linux, Windows and Mac OSX. Please refer to Docker [installation guideline](https://docs.docker.com/installation) for details.

  * For Windows and Mac systems it is additionally possible
    to use [Kitematic](./kitematic/kitematic.md) and launch
    Galaxy GraphClust using the OS graphical user interface.

  * Alternatively Galaxy-GraphClust can be integrated into a running Galaxy server. All the Galaxy-GraphClust tools and workflows needed to run the 
    GraphClust pipeline are listed in [workflows](./workflows/) and 
    [tools-list](clip.yml).
    The [Freibug Galaxy Instance](http://galaxy.uni-freiburg.de) for example
    offers next to 700 other tools also the GraphClust Pipeline.


## Running the Galaxy server
#### From the command line (Linux/Windows/MacOS):

```bash
docker run -i -t -p 8080:80 backofenlab/docker-galaxy-clip
```

For more details about this command line or specific usage, please consult the Galaxy Docker [`guide`](https://github.com/bgruening/docker-galaxy-stable/blob/master/README.md).

#### Using graphic interface (Windows/MacOS):
Please check this [step-by-step guide](./kitematic/kitematic.md).

### Demo instance:
A running demo instance of Galaxy-GraphClust is available at http://bit.ly/GalaxyGraphClust.
Please note this instance is exactly the same Docker container which we offer here. It has limited computation 
capacity and intended for demonstration and testing purposes. Currently it is not planned to have a long-time availability. We recommend to follow instructions above.

#### Setup support:
In case you encountered problems please use the recommended settings, check the [FAQs](./FAQ.md) or contact us via [*Issues*](https://github.com/BackofenLab/docker-galaxy-clip/issues). 

#### Recommended settings:
**Galaxy-CLIP has been tested on these operating systems:**
* *Linux*: Kernel 4.2 or higher, preferably with aufs support (see [FAQ](FAQ.md))

**Hardware:**
* Minimum 8GB RAM
* Minimum 20GB Free disk space


#### Setup support:
In case you encountered problems please check the [FAQ page](./FAQ.md) or contact us via [*Issues*](https://github.com/BackofenLab/docker-galaxy-clip/issues).

# Usage - How to run Galaxy-CLIP:

## Browser access to the server:
After running the Galaxy server, a web server is established under the host IP/URL and designated port (default 8080).

* Inside your browser goto IP/URL:PORT
* Following same settings as previous step

  * In the **same local computer**: [http://localhost:8080/](http://localhost:8080)
  * In **any computer with network connection to the host**: [http://HOSTIP:8080]()

## Help

### Interactive tours
Interactive Tours are available for Galaxy and Galaxy-CLIP. To run the tours please on top panel go to **Help→Interactive Tours** and click on one of the tours prefixed **CLIP:**. You can check the other tours for a more general introduction to the Galaxy interface.

### Import or upload a workflow

To import or upload an existing workflow, on the top panel go to the **Workflow** menu. On top right side of the screen click on **Upload or import workflow** button. You can either upload a workflow from your local system or by providing the URL of the workflow. To have access to the workflow menu you must be logged in.


#### [Frequently Asked Questions](FAQ.md) 

CLIP pipeline overview
===============================

mapping
peak calling
statistical evaluation
motif finding (?)

# Contributors

 - [Torsten Houwaart](https://github.com/torhou/)
 - [Zaher Wanli](https://github.com/zwanli)
 - [Bjoern Gruening](https://github.com/bgruening)


# Support & Bug Reports

You can file an [github issue](https://github.com/BackofenLab/docker-galaxy-clip/issues) or ask us on the [Galaxy development list](http://lists.bx.psu.edu/listinfo/galaxy-dev).

# Publications

[T. Houwaart, Z. Wanli, P. Wright, R. Backofen and B. Gruening, Galaxy-CLIP: Environment for CLIP-seq data analyses, submitted] 
[M. Uhl, T. Houwaart, G. Corrado, P. Wright, R. Backofen, Computational analysis of CLIP-seq data, doi:10.1016/j.ymeth.2017.02.006]
