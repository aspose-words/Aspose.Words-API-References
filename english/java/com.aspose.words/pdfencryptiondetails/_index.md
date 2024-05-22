---
title: PdfEncryptionDetails
linktitle: PdfEncryptionDetails
second_title: Aspose.Words for Java
description: Contains details for encrypting and access permissions for a PDF document in Java.
type: docs
weight: 492
url: /java/com.aspose.words/pdfencryptiondetails/
---

**Inheritance:**
java.lang.Object
```
public class PdfEncryptionDetails
```

Contains details for encrypting and access permissions for a PDF document.

To learn more, visit the [ Protect or Encrypt a Document ][Protect or Encrypt a Document] documentation article.

 **Examples:** 

Shows how to set permissions on a saved PDF document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Hello world!");

 // Extend permissions to allow the editing of annotations.
 PdfEncryptionDetails encryptionDetails =
         new PdfEncryptionDetails("password", "", PdfPermissions.MODIFY_ANNOTATIONS | PdfPermissions.DOCUMENT_ASSEMBLY);

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions saveOptions = new PdfSaveOptions();

 // Enable encryption via the "EncryptionDetails" property.
 saveOptions.setEncryptionDetails(encryptionDetails);

 // When we open this document, we will need to provide the password before accessing its contents.
 doc.save(getArtifactsDir() + "PdfSaveOptions.EncryptionPermissions.pdf", saveOptions);
 
```


[Protect or Encrypt a Document]: https://docs.aspose.com/words/java/protect-or-encrypt-a-document/
## Constructors

| Constructor | Description |
| --- | --- |
| [PdfEncryptionDetails(String userPassword, String ownerPassword)](#PdfEncryptionDetails-java.lang.String-java.lang.String) | Initializes an instance of this class. |
| [PdfEncryptionDetails(String userPassword, String ownerPassword, int permissions)](#PdfEncryptionDetails-java.lang.String-java.lang.String-int) | Initializes a new instance of this class. |
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

### PdfEncryptionDetails(String userPassword, String ownerPassword, int permissions) {#PdfEncryptionDetails-java.lang.String-java.lang.String-int}
```
public PdfEncryptionDetails(String userPassword, String ownerPassword, int permissions)
```


Initializes a new instance of this class.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| userPassword | java.lang.String |  |
| ownerPassword | java.lang.String |  |
| permissions | int |  |

### getOwnerPassword() {#getOwnerPassword}
```
public String getOwnerPassword()
```


Specifies the owner password for the encrypted PDF document.

 **Remarks:** 

The owner password allows the user to open an encrypted PDF document without any access restrictions specified in [getPermissions()](../../com.aspose.words/pdfencryptiondetails/\#getPermissions) / [setPermissions(int)](../../com.aspose.words/pdfencryptiondetails/\#setPermissions-int).

The owner password cannot be the same as the user password.

 **Examples:** 

Shows how to set permissions on a saved PDF document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Hello world!");

 // Extend permissions to allow the editing of annotations.
 PdfEncryptionDetails encryptionDetails =
         new PdfEncryptionDetails("password", "", PdfPermissions.MODIFY_ANNOTATIONS | PdfPermissions.DOCUMENT_ASSEMBLY);

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions saveOptions = new PdfSaveOptions();

 // Enable encryption via the "EncryptionDetails" property.
 saveOptions.setEncryptionDetails(encryptionDetails);

 // When we open this document, we will need to provide the password before accessing its contents.
 doc.save(getArtifactsDir() + "PdfSaveOptions.EncryptionPermissions.pdf", saveOptions);
 
```

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### getPermissions() {#getPermissions}
```
public int getPermissions()
```


Specifies the operations that are allowed to a user on an encrypted PDF document. The default value is [PdfPermissions.DISALLOW\_ALL](../../com.aspose.words/pdfpermissions/\#DISALLOW-ALL).

 **Examples:** 

Shows how to set permissions on a saved PDF document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Hello world!");

 // Extend permissions to allow the editing of annotations.
 PdfEncryptionDetails encryptionDetails =
         new PdfEncryptionDetails("password", "", PdfPermissions.MODIFY_ANNOTATIONS | PdfPermissions.DOCUMENT_ASSEMBLY);

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions saveOptions = new PdfSaveOptions();

 // Enable encryption via the "EncryptionDetails" property.
 saveOptions.setEncryptionDetails(encryptionDetails);

 // When we open this document, we will need to provide the password before accessing its contents.
 doc.save(getArtifactsDir() + "PdfSaveOptions.EncryptionPermissions.pdf", saveOptions);
 
```

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

 **Examples:** 

Shows how to set permissions on a saved PDF document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Hello world!");

 // Extend permissions to allow the editing of annotations.
 PdfEncryptionDetails encryptionDetails =
         new PdfEncryptionDetails("password", "", PdfPermissions.MODIFY_ANNOTATIONS | PdfPermissions.DOCUMENT_ASSEMBLY);

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions saveOptions = new PdfSaveOptions();

 // Enable encryption via the "EncryptionDetails" property.
 saveOptions.setEncryptionDetails(encryptionDetails);

 // When we open this document, we will need to provide the password before accessing its contents.
 doc.save(getArtifactsDir() + "PdfSaveOptions.EncryptionPermissions.pdf", saveOptions);
 
```

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

 **Examples:** 

Shows how to set permissions on a saved PDF document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Hello world!");

 // Extend permissions to allow the editing of annotations.
 PdfEncryptionDetails encryptionDetails =
         new PdfEncryptionDetails("password", "", PdfPermissions.MODIFY_ANNOTATIONS | PdfPermissions.DOCUMENT_ASSEMBLY);

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions saveOptions = new PdfSaveOptions();

 // Enable encryption via the "EncryptionDetails" property.
 saveOptions.setEncryptionDetails(encryptionDetails);

 // When we open this document, we will need to provide the password before accessing its contents.
 doc.save(getArtifactsDir() + "PdfSaveOptions.EncryptionPermissions.pdf", saveOptions);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### setPermissions(int value) {#setPermissions-int}
```
public void setPermissions(int value)
```


Specifies the operations that are allowed to a user on an encrypted PDF document. The default value is [PdfPermissions.DISALLOW\_ALL](../../com.aspose.words/pdfpermissions/\#DISALLOW-ALL).

 **Examples:** 

Shows how to set permissions on a saved PDF document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Hello world!");

 // Extend permissions to allow the editing of annotations.
 PdfEncryptionDetails encryptionDetails =
         new PdfEncryptionDetails("password", "", PdfPermissions.MODIFY_ANNOTATIONS | PdfPermissions.DOCUMENT_ASSEMBLY);

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions saveOptions = new PdfSaveOptions();

 // Enable encryption via the "EncryptionDetails" property.
 saveOptions.setEncryptionDetails(encryptionDetails);

 // When we open this document, we will need to provide the password before accessing its contents.
 doc.save(getArtifactsDir() + "PdfSaveOptions.EncryptionPermissions.pdf", saveOptions);
 
```

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

 **Examples:** 

Shows how to set permissions on a saved PDF document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Hello world!");

 // Extend permissions to allow the editing of annotations.
 PdfEncryptionDetails encryptionDetails =
         new PdfEncryptionDetails("password", "", PdfPermissions.MODIFY_ANNOTATIONS | PdfPermissions.DOCUMENT_ASSEMBLY);

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions saveOptions = new PdfSaveOptions();

 // Enable encryption via the "EncryptionDetails" property.
 saveOptions.setEncryptionDetails(encryptionDetails);

 // When we open this document, we will need to provide the password before accessing its contents.
 doc.save(getArtifactsDir() + "PdfSaveOptions.EncryptionPermissions.pdf", saveOptions);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

