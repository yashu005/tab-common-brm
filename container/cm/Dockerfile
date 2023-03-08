# Copyright (c) 2021 Oracle Corporation and/or its affiliates. All rights reserved.
###
## This is the Dockerfile for cne/brm/cm
##
## REQUIRED FILES TO BUILD THIS IMAGE
## ----------------------------------
##  The output from the binary build stage 1 should be available in the same folder as the Dockerfile.
##  This dockerfile conforms to the binary stage 1 output format for where to load files from
##
## HOW TO BUILD THIS IMAGE - Developers
## ------------------------------------
## $ Execute "make build" command in the same directory where Dockerfile and Makefile is present
## 
###

ARG BASE_IMAGE=cm
#ARG BASE_TAG=12.0.0.7.0
#Below is BRM_IP22 DIGI###########
ARG BASE_TAG=12.0.0.7.0-35009568
#Below is BRM_IP14 DIGI###########
#ARG BASE_TAG=12.0.0.7.0-34916707
#Below is BRM_IP3 DIGI############
#ARG BASE_TAG=12.0.0.7.0-34709207
#ARG BASE_TAG=12.0.0.6.0-34428362
#IP4
#ARG BASE_TAG=12.0.0.7.0-34763817
#ARG BASE_TAG=12.0.0.7.0-34627512
#ARG BASE_TAG=12.0.0.7.0-34623054
#ARG BASE_TAG=12.0.0.7.0-34658850
#IP7
#ARG BASE_TAG=12.0.0.7.0-34833129
#IP12
#ARG BASE_TAG=12.0.0.7.0-34858379
#IP8
#ARG BASE_TAG=12.0.0.7.0-34834534
#Latest Patch TP/DTAC
#ARG BASE_TAG=12.0.0.7.0-35071119
#ARG BASE_TAG=12.0.0.7.0-34951118
#ARG BASE_TAG=12.0.0.7.0-34968056
#ARG BASE_TAG=12.0.0.7.0-35071119
#latest Patch TP
#ARG BASE_TAG=12.0.0.7.0-34990322
#ARG BASE_TAG=12.0.0.7.0-34968043
#ARG BASE_TAG=12.0.0.7.0-35009568
#ARG BASE_TAG=12.0.0.7.0-35071119

FROM ${BASE_IMAGE}:${BASE_TAG}

LABEL "org.opencontainers.image.authors"="Oracle Communications Applications Consulting (OCAC)"
LABEL "org.opencontainers.image.title"="TAB Common image: common/brm/cm"
LABEL "org.opencontainers.image.description"="Extension for Oracle Communications BRM image - cm"

USER root

# TODO: May be better to change this so that in the make file we create the required copy list and then create a single layer
# TODO: Doing that will require an external metadata model to be created to control what happens in the Dockerfile, so adds complexity

COPY --chown=omsuser:root brm/lib/fm_tab_utils_common.so             ${PIN_HOME}/custom/lib/fm_tab_utils_common.so
COPY --chown=omsuser:root brm/lib/fm_tab_utils_common_pol.so         ${PIN_HOME}/custom/lib/fm_tab_utils_common_pol.so
COPY --chown=omsuser:root brm/lib/fm_tab_cust.so                     ${PIN_HOME}/custom/lib/fm_tab_cust.so
COPY --chown=omsuser:root brm/lib/fm_tab_cust_pol.so                 ${PIN_HOME}/custom/lib/fm_tab_cust_pol.so
COPY --chown=omsuser:root brm/lib/fm_tab_subscription.so             ${PIN_HOME}/custom/lib/fm_tab_subscription.so
COPY --chown=omsuser:root brm/lib/fm_tab_subscription_pol.so         ${PIN_HOME}/custom/lib/fm_tab_subscription_pol.so
COPY --chown=omsuser:root brm/lib/fm_cust_pol_common.so              ${PIN_HOME}/custom/lib/fm_cust_pol_common.so
COPY --chown=omsuser:root brm/lib/fm_tab_notify_pol.so               ${PIN_HOME}/custom/lib/fm_tab_notify_pol.so
COPY --chown=omsuser:root brm/lib/fm_tab_ar.so                       ${PIN_HOME}/custom/lib/fm_tab_ar.so
COPY --chown=omsuser:root brm/lib/fm_tab_ar_pol.so                   ${PIN_HOME}/custom/lib/fm_tab_ar_pol.so
COPY --chown=omsuser:root brm/lib/fm_tab_bill.so                     ${PIN_HOME}/custom/lib/fm_tab_bill.so
COPY --chown=omsuser:root brm/lib/fm_tab_bill_pol.so                 ${PIN_HOME}/custom/lib/fm_tab_bill_pol.so
COPY --chown=omsuser:root brm/lib/fm_tab_mig.so                      ${PIN_HOME}/custom/lib/fm_tab_mig.so
COPY --chown=omsuser:root brm/lib/fm_tab_collections.so		     ${PIN_HOME}/custom/lib/fm_tab_collections.so
COPY --chown=omsuser:root brm/lib/fm_tab_collections_pol.so  	     ${PIN_HOME}/custom/lib/fm_tab_collections_pol.so
COPY --chown=omsuser:root brm/lib/tab_ops_flds                       ${PIN_HOME}/custom/lib/tab_ops_flds

RUN chmod -R 755 "${PIN_HOME}"/custom/lib/*

USER omsuser
