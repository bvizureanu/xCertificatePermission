# xCertificatePermission
PowerShell DSC module for setting permissions on private keys of certificates.

## Installation

### From GitHub source code

To manually install the module, download the source code from GitHub and unzip
the contents to the '$env:ProgramFiles\WindowsPowerShell\Modules' folder.

## Change log

A full list of changes in each version can be found in the [change log](CHANGELOG.md).

## Resources

* [**xCertificatePermission**](#xcertificatepermission)
  resource to grant a user permission to read the private key of a certificate.
  
### xCertificatePermission

This resource is used to create, remove, and update an Always On Availability Group.
It will also manage the Availability Group replica on the specified node.

#### Requirements

* Target machine must be running Windows Server 2008 R2 or later.

#### Parameters

* **`[String]` Location** _(Key)_: Location of the certificate store. { LocalMachine | CurrentUser }
* **`[String]` Thumbprint** _(Key)_: Thumbprint of the certificate.
* **`[String]` Store** _(Key)_: Name of the store within the Location the certificate exists.
* **`[String]` Ensure** _(Write)_: Specifies if the permission should be present
  or absent. { Present | Absent }
* **`[String]` UserAccount** _(Write)_: User account to assign the permission to.
* **`[String]` Permission** _(Write)_: Permission to assign or remove. { Read | FullControl}

#### Examples
* 