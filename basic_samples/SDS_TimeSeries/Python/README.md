# Building a Python client to make REST API calls to the SDS Service

[![Build Status](https://dev.azure.com/osieng/engineering/_apis/build/status/product-readiness/OCS/SDS_TS_Python?branchName=master)](https://dev.azure.com/osieng/engineering/_build/latest?definitionId=927&branchName=master)

The sample code in this topic demonstrates how to invoke SDS REST APIs using Python. By examining the code, you will see how to create an SdsType and SdsStream, and how to create, read, update, and delete values in SDS. You will also see the effect of the accept verbosity header, summaries value call, and how to do bulk streams calls.

This sample code uses the python `requests` module, which natively supports encoding. As a result, the requests in this sample will automatically include the `Accept-Encoding` header and automatically decompress the encoded responses before returning them to the user, so no special handling is required to support compression.

The sections that follow provide a brief description of the process from beginning to end.

Developed against Python 3.7.2.

## To Run this Sample:

1. Clone the GitHub repository
1. Install required modules: `pip install -r requirements.txt`
1. Open the folder with your favorite IDE
1. Update `config.ini` with the credentials provided by OSIsoft
1. Run `program.py`

To Test the sample:

1. Run `python test.py`

or

1. Install pytest `pip install pytest`
1. Run `pytest program.py`

## Configure the Sample:

Included in the sample there is a configuration file with placeholders that need to be replaced with the proper values. They include information for authentication, connecting to the SDS Service, and pointing to a namespace.

The values to be replaced are in `config.ini`:

```ini
[Configurations]
Namespace = Samples

[Access]
Resource = https://dat-b.osisoft.com
Tenant = REPLACE_WITH_TENANT_ID
ApiVersion = v1

[Credentials]
ClientId = REPLACE_WITH_APPLICATION_IDENTIFIER
ClientSecret = REPLACE_WITH_APPLICATION_SECRET
```

---

Automated test uses Python 3.6.8 x64

Complete dependencies listed in [DEPENDENCIES.md](DEPENDENCIES.md)

For the general steps or switch languages see the Task [ReadMe](../../../)  
For the main OCS page [ReadMe](https://github.com/osisoft/OSI-Samples-OCS)  
For the main samples page on master [ReadMe](https://github.com/osisoft/OSI-Samples)
