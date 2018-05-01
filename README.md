# Dotmesh S3 API

**STATUS: What you currently see here is WIP, do not use in production!** 

This is the S3 API for Dotmesh.

It provides for an S3 server exposing and managing a local filesystem as an S3 service in V3. 

Note: the [Minio Go client](https://docs.minio.io/docs/golang-client-api-reference) can be used as a client for testing.

## Design

For the initial iteration, we are making the following assumptions:

- The here provided S3 API is just one way to access it, that is, someone else may access the same data using, for example, via the `dm` CLI
- An S3 bucket is represented in Dotmesh via a dot
- There exists a unique mapping for object names (since they might be in a sub-directory and the path needs to be made part of the name)

## Operations

The supported operations are:

Bucket-level:

- `List` … lists all buckets
- `Exists` … checks if a bucket exists
- `Create` … creates a bucket
- `Remove` … removes a bucket
- `Objects` … lists objects in a bucket

Object-level:

- `Get` … returns a stream of the object data
- `Put` … uploads object data
- `Remove` … removes object data

