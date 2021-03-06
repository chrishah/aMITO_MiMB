
This Docker image is a self contained environment to run the tutorial detailed in the article __Assembly of ancient mitochondrial genomes without a closely related reference sequence__ by Christoph Hahn in __Ancient DNA: Methods and Protocols, Second Edition__, edited by __Shapiro B., Hofreiter M., Rodrigues Soares A.E., Heintzman P.D., Paijmans L.A., and Barlow A.__

The image runs Ubuntu 16.04 and contains the following sofware:
 - MITObim (v.1.9.1)
 - MIRA (v.4.0.2)
 - BLAST+ (v.2.2.31)
 - MUSCLE (v.3.8.31)
 - git (v.2.7.4)
 - perl (v.5.22.1)
 - Python (v.2.7.12)

Start the docker container by doing (might require `sudo`):
```bash
docker run -i -t -v $(pwd):/home/working --rm --net=host chrishah/amito_mimb /bin/bash
```

This will download the image, start up the docker container (you will see the prompt change) and mount the directory `/home/working` (do not change) of the container to your current working directory (`$(pwd)` - change if you want).


CONTACT
-------

Christoph Hahn <christoph.hahn@uni-graz.at>

