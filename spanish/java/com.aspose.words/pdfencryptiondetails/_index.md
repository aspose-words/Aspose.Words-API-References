---
title: "PdfEncryptionDetails"
linktitle: "PdfEncryptionDetails"
second_title: "Aspose.Words para Java"
description: "Contiene detalles para el cifrado y los permisos de acceso de un documento PDF en Java."
type: docs
weight: 534
url: /es/java/com.aspose.words/pdfencryptiondetails/
---

**Inheritance:**
java.lang.Object
```
public class PdfEncryptionDetails
```

Contiene detalles para el cifrado y los permisos de acceso de un documento PDF.

Para obtener más información, visite el artículo de documentación [ Protect or Encrypt a Document ][Protect or Encrypt a Document].

 **Examples:** 

Muestra cómo establecer permisos en un documento PDF guardado.

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
## Constructores

| Constructor | Descripción |
| --- | --- |
| [PdfEncryptionDetails(String userPassword, String ownerPassword)](#PdfEncryptionDetails-java.lang.String-java.lang.String) | Inicializa una instancia de esta clase. |
| [PdfEncryptionDetails(String userPassword, String ownerPassword, int permissions)](#PdfEncryptionDetails-java.lang.String-java.lang.String-int) | Inicializa una nueva instancia de esta clase. |
## Métodos

| Método | Descripción |
| --- | --- |
| [getOwnerPassword()](#getOwnerPassword) | Especifica la contraseña del propietario para el documento PDF cifrado. |
| [getPermissions()](#getPermissions) | Especifica las operaciones que se permiten a un usuario en un documento PDF cifrado. |
| [getUserPassword()](#getUserPassword) | Especifica la contraseña de usuario requerida para abrir el documento PDF cifrado. |
| [setOwnerPassword(String value)](#setOwnerPassword-java.lang.String) | Especifica la contraseña del propietario para el documento PDF cifrado. |
| [setPermissions(int value)](#setPermissions-int) | Especifica las operaciones que se permiten a un usuario en un documento PDF cifrado. |
| [setUserPassword(String value)](#setUserPassword-java.lang.String) | Especifica la contraseña de usuario requerida para abrir el documento PDF cifrado. |
### PdfEncryptionDetails(String userPassword, String ownerPassword) {#PdfEncryptionDetails-java.lang.String-java.lang.String}
```
public PdfEncryptionDetails(String userPassword, String ownerPassword)
```


Inicializa una instancia de esta clase.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| userPassword | java.lang.String |  |
| ownerPassword | java.lang.String |  |

### PdfEncryptionDetails(String userPassword, String ownerPassword, int permissions) {#PdfEncryptionDetails-java.lang.String-java.lang.String-int}
```
public PdfEncryptionDetails(String userPassword, String ownerPassword, int permissions)
```


Inicializa una nueva instancia de esta clase.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| userPassword | java.lang.String |  |
| ownerPassword | java.lang.String |  |
| permissions | int |  |

### getOwnerPassword() {#getOwnerPassword}
```
public String getOwnerPassword()
```


Especifica la contraseña del propietario para el documento PDF cifrado.

 **Remarks:** 

La contraseña del propietario permite al usuario abrir un documento PDF cifrado sin ninguna restricción de acceso especificada en [getPermissions()](../../com.aspose.words/pdfencryptiondetails/\#getPermissions) / [setPermissions(int)](../../com.aspose.words/pdfencryptiondetails/\#setPermissions-int).

La contraseña del propietario no puede ser la misma que la contraseña de usuario.

 **Examples:** 

Muestra cómo establecer permisos en un documento PDF guardado.

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
java.lang.String - El valor java.lang.String correspondiente.
### getPermissions() {#getPermissions}
```
public int getPermissions()
```


Especifica las operaciones que se permiten a un usuario en un documento PDF cifrado. El valor predeterminado es [PdfPermissions.DISALLOW\_ALL](../../com.aspose.words/pdfpermissions/\#DISALLOW-ALL).

 **Examples:** 

Muestra cómo establecer permisos en un documento PDF guardado.

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
int - El valor int correspondiente. El valor devuelto es una combinación bit a bit de las constantes [PdfPermissions](../../com.aspose.words/pdfpermissions/).
### getUserPassword() {#getUserPassword}
```
public String getUserPassword()
```


Especifica la contraseña de usuario requerida para abrir el documento PDF cifrado.

 **Remarks:** 

Se requerirá la contraseña de usuario para abrir un documento PDF cifrado para su visualización. Los permisos especificados en [getPermissions()](../../com.aspose.words/pdfencryptiondetails/\#getPermissions) / [setPermissions(int)](../../com.aspose.words/pdfencryptiondetails/\#setPermissions-int) serán aplicados por el software lector.

La contraseña de usuario puede ser  null  o una cadena vacía; en este caso no se requerirá contraseña al usuario al abrir el documento PDF. La contraseña de usuario no puede ser la misma que la contraseña del propietario.

 **Examples:** 

Muestra cómo establecer permisos en un documento PDF guardado.

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
java.lang.String - El valor java.lang.String correspondiente.
### setOwnerPassword(String value) {#setOwnerPassword-java.lang.String}
```
public void setOwnerPassword(String value)
```


Especifica la contraseña del propietario para el documento PDF cifrado.

 **Remarks:** 

La contraseña del propietario permite al usuario abrir un documento PDF cifrado sin ninguna restricción de acceso especificada en [getPermissions()](../../com.aspose.words/pdfencryptiondetails/\#getPermissions) / [setPermissions(int)](../../com.aspose.words/pdfencryptiondetails/\#setPermissions-int).

La contraseña del propietario no puede ser la misma que la contraseña de usuario.

 **Examples:** 

Muestra cómo establecer permisos en un documento PDF guardado.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | El valor java.lang.String correspondiente. |

### setPermissions(int value) {#setPermissions-int}
```
public void setPermissions(int value)
```


Especifica las operaciones que se permiten a un usuario en un documento PDF cifrado. El valor predeterminado es [PdfPermissions.DISALLOW\_ALL](../../com.aspose.words/pdfpermissions/\#DISALLOW-ALL).

 **Examples:** 

Muestra cómo establecer permisos en un documento PDF guardado.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | El valor int correspondiente. El valor debe ser una combinación bit a bit de las constantes [PdfPermissions](../../com.aspose.words/pdfpermissions/). |

### setUserPassword(String value) {#setUserPassword-java.lang.String}
```
public void setUserPassword(String value)
```


Especifica la contraseña de usuario requerida para abrir el documento PDF cifrado.

 **Remarks:** 

Se requerirá la contraseña de usuario para abrir un documento PDF cifrado para su visualización. Los permisos especificados en [getPermissions()](../../com.aspose.words/pdfencryptiondetails/\#getPermissions) / [setPermissions(int)](../../com.aspose.words/pdfencryptiondetails/\#setPermissions-int) serán aplicados por el software lector.

La contraseña de usuario puede ser  null  o una cadena vacía; en este caso no se requerirá contraseña al usuario al abrir el documento PDF. La contraseña de usuario no puede ser la misma que la contraseña del propietario.

 **Examples:** 

Muestra cómo establecer permisos en un documento PDF guardado.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | El valor java.lang.String correspondiente. |

