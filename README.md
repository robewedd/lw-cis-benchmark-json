# Overview

[![Git](https://app.soluble.cloud/api/v1/public/badges/c7bdac96-ceed-4728-8637-ff2459ca45a8.svg?orgId=251133511671)](https://app.soluble.cloud/repos/details/github.com/robewedd/lw-cis-benchmark-json?orgId=251133511671)  

This repo provides example JSON body sections to enable and disable the CIS Benchmarks for GCP & Azure in Lacework when calling the PATCH method on *https://lacework-tenant.lacework.net/api/v1/external/recommendations/gcp* and *https://lacework-tenant.lacework.net/api/v1/external/recommendations/azure* API Endpoints

# Script
This repo also includes an example script that can be used to perform the config, with a requirement of having curl and the Lacework CLI installed.  Usage is:

`cis-config.sh [disable_cis_10|disable_cis_12|enable_cis_12|disable_cis_azure|enable_cis_azure] [lacework-tenant] [lacework-subaccount]`

Where the first argument is the action you wish to perform, the second argument is your lacework tenant (without the `.lacework.net`) and the third argument is the subaccount where the GCP for Lacework is configured.

# Further information

`lacework-tenant` If you are in the Frankfurt datacenter you need to specify this as `tenant.fra`

`lacework-subaccount` If you Lacework tenant is enrolled in an organization then you need to specify the name of the subaccount. If this is not the case then ignore the third argument.
