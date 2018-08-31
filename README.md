# aMITO_MiMB


This repository contains material and instructions for the tutorial detailed in the article 'Assembly of ancient mitochondrial genomes without a closely related reference sequence' by Christoph Hahn in 'Ancient DNA: Methods and Protocols, Second Edition, edited by Shapiro B., Hofreiter M., Rodrigues Soares A.E., Heintzman P.D., Paijmans L.A., and Barlow A.


For the tutorial we have prepared a [Docker](https://www.docker.com/) image (see [here](https://registry.hub.docker.com/u/chrishah/amito_mimb/)). Find out what docker is [here](https://www.docker.com/whatisdocker/). The image contains a stripped down version of Ubuntu 16.04 and all necessary executables and dependencies to run the tutorial. Docker is compatible with all major operating systems, including Mac OSX and Windows (see [here](https://docs.docker.com/installation/#installation)). The image has been tested on Ubuntu, but it should work without problem in any other system where docker was successfully installed.


Start the docker container by doing (might require `sudo`):
```bash
docker run -i -t -v $(pwd):/home/working --rm --net=host chrishah/amito_mimb /bin/bash
```

This will download the image, start up the docker container (you will see the prompt change) and mount it to your current working directory.

**NOTE** that the first startup may take a couple of minutes because the above command will first download the image from [docker hub](https://registry.hub.docker.com/u/chrishah/mitobim/). Subsequent launches will take only seconds.


