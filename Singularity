BootStrap: docker
From: python:2.7.15

%labels
    SDSC_IMG_MAINTAINER hpcdevops
    SDSC_IMG_NAME cloudmesh.client
    SDSC_IMG_DESC Python 2.7.15 Base Image w/ Cloudmesh CMD5 Client for Comet
    SDSC_IMG_VENDOR SDSC HPC Group

%runscript
    exec /usr/local/bin/cms "$@"

%test
    cms version

%post

    # Add cloudmesh tool...
    pip install cloudmesh.comet

    # build info
    echo "Timestamp:" `date --utc` | tee /image-build-info.txt
