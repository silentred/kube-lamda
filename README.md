# Serverless Operator for Kubernetes

## Usage

- write you own handler file
- configure name and visit-path to the service
- post two files to the opterator

## Design

Once operator receives the handler and config file, it does the following things.

- create local path from repo/name in GOPATH
- use template to generate the main function
- build and make docker image, then push the image to a repository
- generate deployment file in yaml
- deploy it the image to k8s

