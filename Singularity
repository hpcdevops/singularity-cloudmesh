BootStrap: docker
From: python:2.7.13

%labels
    SDSC_IMG_MAINTAINER hpcdevops
    SDSC_IMG_NAME cloudmesh_client
    SDSC_IMG_DESC Python 2.7.13 Base Image w/ Cloudmesh Client
    SDSC_IMG_VENDOR SDSC HPC Group

%runscript
    exec /usr/bin/python "$@"

%test
    cm version

%post

    # Add cloudmesh tool...
    pip install cloudmesh_client

    # build info
    echo "Timestamp:" `date --utc` | tee /image-build-info.txt
