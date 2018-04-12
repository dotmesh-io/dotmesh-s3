# Dotmesh S3 API

**STATUS: What you currently see here is WIP, do not use in production!** 

This is the S3 API for Dotmesh.

It provides for an S3 server exposing and managing a local filesystem as an S3 service in V3. 

Note: the [Minio Go client](https://docs.minio.io/docs/golang-client-api-reference) can be used as a client for testing.

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

