# Copyright (c) 2022 Oracle and/or its affiliates.
###
## This is the Dockerfile for cne/brm/brm_apps
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
ARG BASE_IMAGE=brm_apps
#ARG BASE_TAG=12.0.0.7.0
#DIGI specific IP10
#ARG BASE_TAG=12.0.0.7.0-34856808
#DIGI specific IP NEW
ARG BASE_TAG=12.0.0.7.0-34934113
FROM ${BASE_IMAGE}:${BASE_TAG}

LABEL "org.opencontainers.image.authors"="Oracle Communications Applications Consulting (OCAC)"
LABEL "org.opencontainers.image.title"="TAB Common image: common/brm/brm_apps"
LABEL "org.opencontainers.image.description"="Extension for Oracle Communications BRM image - brm_apps"


