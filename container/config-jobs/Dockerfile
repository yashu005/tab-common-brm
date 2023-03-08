# Copyright (c) 2022 Oracle and/or its affiliates.
###
## This is the Dockerfile for cne/brm/config_jobs
##
## REQUIRED FILES TO BUILD THIS IMAGE
## ----------------------------------
## N/A
##
## HOW TO BUILD THIS IMAGE
## -----------------------
## $ Execute "make build" command in the same directory where Dockerfile and Makefile is present
##
###
ARG BASE_IMAGE=config_jobs
#ARG BASE_TAG=12.0.0.7.0
#ARG BASE_TAG=12.0.0.6.0-34428362
#Below is the DIGI IP4################
ARG BASE_TAG=12.0.0.7.0-34763817
#ARG BASE_TAG=12.0.0.7.0-34627512
#ARG BASE_TAG=12.0.0.6.0-34428362
#Below is the DIGI IP2################
#ARG BASE_TAG=12.0.0.7.0-34658850
#Below is the latest CPU patch(FEB)
#ARG BASE_TAG=12.0.0.7.0-34943526
FROM ${BASE_IMAGE}:${BASE_TAG}

LABEL "org.opencontainers.image.authors"="Oracle Communications Applications Consulting (OCAC)"
LABEL "org.opencontainers.image.title"="TAB Common image: common/brm/config_jobs"
LABEL "org.opencontainers.image.description"="Extension for Oracle Communications BRM image - config_jobs"

USER root

COPY --chown=omsuser:root brm/lib/tab_ops_flds                       ${PIN_HOME}/custom/lib/tab_ops_flds

RUN chmod 755 "${PIN_HOME}/custom/lib/tab_ops_flds"

USER omsuser
