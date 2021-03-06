.. _minio-TLS:

==============================
MinIO Transport Layer Security
==============================

.. default-domain:: minio

.. contents:: Table of Contents
   :local:
   :depth: 1

Overview
--------

The MinIO server supports enabling TLS encryption of incoming and outgoing
traffic. MinIO recommends all MinIO servers run with TLS enabled to ensure
end-to-end security of client-server or server-server transmissions.

The MinIO server looks for a private key ``private.key`` and public certificate
``public.crt`` in the following directories:

- **Linux/OSX** : ``${HOME}/.minio/certs``

- **Windows** : ``%%USERPROFILE%%\.minio\certs``

MinIO only supports keys and certificates in the PEM format.

You can customize the certificate directory by passing the ``--certs-dir``
option to ``minio server``. The ``certs`` directory must also include any
intermediate certificates required to establish a chain of trust to the root CA.

For more information, see 
:minio-git:`How to secure access to MinIO server with TLS 
<minio/tree/master/docs/tls>`. 