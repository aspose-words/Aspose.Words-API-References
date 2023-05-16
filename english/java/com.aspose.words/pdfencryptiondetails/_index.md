---
title: PdfEncryptionDetails
linktitle: PdfEncryptionDetails
second_title: Aspose.Words for Java
description: Contains details for encrypting and access permissions for a PDF document in Java.
type: docs
weight: 471
url: /java/com.aspose.words/pdfencryptiondetails/
---

**Inheritance:**
java.lang.Object
```
public class PdfEncryptionDetails
```

Contains details for encrypting and access permissions for a PDF document.

To learn more, visit the [ Protect or Encrypt a Document ][Protect or Encrypt a Document] documentation article.


[Protect or Encrypt a Document]: https://docs.aspose.com/words/java/protect-or-encrypt-a-document/
## Constructors

| Constructor | Description |
| --- | --- |
| [PdfEncryptionDetails(String userPassword, String ownerPassword)](#PdfEncryptionDetails-java.lang.String-java.lang.String) | Initializes an instance of this class. |
## Methods

| Method | Description |
| --- | --- |
| [getOwnerPassword()](#getOwnerPassword) | Specifies the owner password for the encrypted PDF document. |
| [getPermissions()](#getPermissions) | Specifies the operations that are allowed to a user on an encrypted PDF document. |
| [getUserPassword()](#getUserPassword) | Specifies the user password required for opening the encrypted PDF document. |
| [setOwnerPassword(String value)](#setOwnerPassword-java.lang.String) | Specifies the owner password for the encrypted PDF document. |
| [setPermissions(int value)](#setPermissions-int) | Specifies the operations that are allowed to a user on an encrypted PDF document. |
| [setUserPassword(String value)](#setUserPassword-java.lang.String) | Specifies the user password required for opening the encrypted PDF document. |
### PdfEncryptionDetails(String userPassword, String ownerPassword) {#PdfEncryptionDetails-java.lang.String-java.lang.String}
```
public PdfEncryptionDetails(String userPassword, String ownerPassword)
```


Initializes an instance of this class.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| userPassword | java.lang.String |  |
| ownerPassword | java.lang.String |  |

### getOwnerPassword() {#getOwnerPassword}
```
public String getOwnerPassword()
```


Specifies the owner password for the encrypted PDF document.

 **Remarks:** 

The owner password allows the user to open an encrypted PDF document without any access restrictions specified in [getPermissions()](../../com.aspose.words/pdfencryptiondetails/\#getPermissions) / [setPermissions(int)](../../com.aspose.words/pdfencryptiondetails/\#setPermissions-int).

The owner password cannot be the same as the user password.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### getPermissions() {#getPermissions}
```
public int getPermissions()
```


Specifies the operations that are allowed to a user on an encrypted PDF document. The default value is [PdfPermissions.DISALLOW\_ALL](../../com.aspose.words/pdfpermissions/\#DISALLOW-ALL).

**Returns:**
int - The corresponding  int  value. The returned value is a bitwise combination of [PdfPermissions](../../com.aspose.words/pdfpermissions/) constants.
### getUserPassword() {#getUserPassword}
```
public String getUserPassword()
```


Specifies the user password required for opening the encrypted PDF document.

 **Remarks:** 

The user password will be required to open an encrypted PDF document for viewing. The permissions specified in [getPermissions()](../../com.aspose.words/pdfencryptiondetails/\#getPermissions) / [setPermissions(int)](../../com.aspose.words/pdfencryptiondetails/\#setPermissions-int) will be enforced by the reader software.

The user password can be  null  or empty string, in this case no password will be required from the user when opening the PDF document. The user password cannot be the same as the owner password.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### setOwnerPassword(String value) {#setOwnerPassword-java.lang.String}
```
public void setOwnerPassword(String value)
```


Specifies the owner password for the encrypted PDF document.

 **Remarks:** 

The owner password allows the user to open an encrypted PDF document without any access restrictions specified in [getPermissions()](../../com.aspose.words/pdfencryptiondetails/\#getPermissions) / [setPermissions(int)](../../com.aspose.words/pdfencryptiondetails/\#setPermissions-int).

The owner password cannot be the same as the user password.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### setPermissions(int value) {#setPermissions-int}
```
public void setPermissions(int value)
```


Specifies the operations that are allowed to a user on an encrypted PDF document. The default value is [PdfPermissions.DISALLOW\_ALL](../../com.aspose.words/pdfpermissions/\#DISALLOW-ALL).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be a bitwise combination of [PdfPermissions](../../com.aspose.words/pdfpermissions/) constants. |

### setUserPassword(String value) {#setUserPassword-java.lang.String}
```
public void setUserPassword(String value)
```


Specifies the user password required for opening the encrypted PDF document.

 **Remarks:** 

The user password will be required to open an encrypted PDF document for viewing. The permissions specified in [getPermissions()](../../com.aspose.words/pdfencryptiondetails/\#getPermissions) / [setPermissions(int)](../../com.aspose.words/pdfencryptiondetails/\#setPermissions-int) will be enforced by the reader software.

The user password can be  null  or empty string, in this case no password will be required from the user when opening the PDF document. The user password cannot be the same as the owner password.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

