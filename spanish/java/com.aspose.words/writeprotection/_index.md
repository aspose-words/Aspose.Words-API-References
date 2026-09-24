---
title: "WriteProtection"
linktitle: "WriteProtection"
second_title: "Aspose.Words para Java"
description: "Especifica la configuración de protección contra escritura para un documento en Java."
type: docs
weight: 738
url: /es/java/com.aspose.words/writeprotection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class WriteProtection implements Cloneable
```

Especifica la configuración de protección contra escritura para un documento.

Para obtener más información, visite el artículo de documentación [ Protect or Encrypt a Document ][Protect or Encrypt a Document].

 **Remarks:** 

La protección contra escritura especifica si el autor ha recomendado que el documento se abra como solo lectura y/o requiera una contraseña para modificar un documento.

La protección contra escritura es diferente de la protección de documentos. La protección contra escritura se especifica en Microsoft Word en las opciones del cuadro de diálogo Guardar como.

No crea instancias de esta clase directamente. Accede a la configuración de protección del documento a través de la propiedad [Document.getWriteProtection()](../../com.aspose.words/document/\#getWriteProtection).

 **Examples:** 

Muestra cómo proteger un documento con una contraseña.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world! This document is protected.");
 // Enter a password up to 15 characters in length, and then verify the document's protection status.
 doc.getWriteProtection().setPassword("MyPassword");
 doc.getWriteProtection().setReadOnlyRecommended(true);

 Assert.assertTrue(doc.getWriteProtection().isWriteProtected());
 Assert.assertTrue(doc.getWriteProtection().validatePassword("MyPassword"));

 // Protection does not prevent the document from being edited programmatically, nor does it encrypt the contents.
 doc.save(getArtifactsDir() + "Document.WriteProtection.docx");
 doc = new Document(getArtifactsDir() + "Document.WriteProtection.docx");

 Assert.assertTrue(doc.getWriteProtection().isWriteProtected());

 builder = new DocumentBuilder(doc);
 builder.moveToDocumentEnd();
 builder.writeln("Writing text in a protected document.");

 Assert.assertEquals("Hello world! This document is protected." +
         "\rWriting text in a protected document.", doc.getText().trim());
 
```


[Protect or Encrypt a Document]: https://docs.aspose.com/words/java/protect-or-encrypt-a-document/
## Métodos

| Método | Descripción |
| --- | --- |
| [getReadOnlyRecommended()](#getReadOnlyRecommended) | Especifica si el autor del documento ha recomendado que el documento se abra como solo lectura. |
| [isWriteProtected()](#isWriteProtected) | Devuelve  true  cuando se establece una contraseña de protección contra escritura. |
| [setPassword(String password)](#setPassword-java.lang.String) | Establece la contraseña de protección contra escritura para el documento. |
| [setReadOnlyRecommended(boolean value)](#setReadOnlyRecommended-boolean) | Especifica si el autor del documento ha recomendado que el documento se abra como solo lectura. |
| [validatePassword(String password)](#validatePassword-java.lang.String) | Devuelve  true  si la contraseña especificada es la misma que la contraseña de protección contra escritura con la que se protegió el documento. |
### getReadOnlyRecommended() {#getReadOnlyRecommended}
```
public boolean getReadOnlyRecommended()
```


Especifica si el autor del documento ha recomendado que el documento se abra como solo lectura.

 **Examples:** 

Muestra cómo proteger un documento con una contraseña.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world! This document is protected.");
 // Enter a password up to 15 characters in length, and then verify the document's protection status.
 doc.getWriteProtection().setPassword("MyPassword");
 doc.getWriteProtection().setReadOnlyRecommended(true);

 Assert.assertTrue(doc.getWriteProtection().isWriteProtected());
 Assert.assertTrue(doc.getWriteProtection().validatePassword("MyPassword"));

 // Protection does not prevent the document from being edited programmatically, nor does it encrypt the contents.
 doc.save(getArtifactsDir() + "Document.WriteProtection.docx");
 doc = new Document(getArtifactsDir() + "Document.WriteProtection.docx");

 Assert.assertTrue(doc.getWriteProtection().isWriteProtected());

 builder = new DocumentBuilder(doc);
 builder.moveToDocumentEnd();
 builder.writeln("Writing text in a protected document.");

 Assert.assertEquals("Hello world! This document is protected." +
         "\rWriting text in a protected document.", doc.getText().trim());
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### isWriteProtected() {#isWriteProtected}
```
public boolean isWriteProtected()
```


Devuelve  true  cuando se establece una contraseña de protección contra escritura.

 **Examples:** 

Muestra cómo proteger un documento con una contraseña.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world! This document is protected.");
 // Enter a password up to 15 characters in length, and then verify the document's protection status.
 doc.getWriteProtection().setPassword("MyPassword");
 doc.getWriteProtection().setReadOnlyRecommended(true);

 Assert.assertTrue(doc.getWriteProtection().isWriteProtected());
 Assert.assertTrue(doc.getWriteProtection().validatePassword("MyPassword"));

 // Protection does not prevent the document from being edited programmatically, nor does it encrypt the contents.
 doc.save(getArtifactsDir() + "Document.WriteProtection.docx");
 doc = new Document(getArtifactsDir() + "Document.WriteProtection.docx");

 Assert.assertTrue(doc.getWriteProtection().isWriteProtected());

 builder = new DocumentBuilder(doc);
 builder.moveToDocumentEnd();
 builder.writeln("Writing text in a protected document.");

 Assert.assertEquals("Hello world! This document is protected." +
         "\rWriting text in a protected document.", doc.getText().trim());
 
```

**Returns:**
boolean -  true  cuando se establece una contraseña de protección contra escritura.
### setPassword(String password) {#setPassword-java.lang.String}
```
public void setPassword(String password)
```


Establece la contraseña de protección contra escritura para el documento.

 **Remarks:** 

Si se establece una contraseña, Microsoft Word requerirá que el usuario la introduzca o abra el documento como solo lectura.

 **Examples:** 

Muestra cómo proteger un documento con una contraseña.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world! This document is protected.");
 // Enter a password up to 15 characters in length, and then verify the document's protection status.
 doc.getWriteProtection().setPassword("MyPassword");
 doc.getWriteProtection().setReadOnlyRecommended(true);

 Assert.assertTrue(doc.getWriteProtection().isWriteProtected());
 Assert.assertTrue(doc.getWriteProtection().validatePassword("MyPassword"));

 // Protection does not prevent the document from being edited programmatically, nor does it encrypt the contents.
 doc.save(getArtifactsDir() + "Document.WriteProtection.docx");
 doc = new Document(getArtifactsDir() + "Document.WriteProtection.docx");

 Assert.assertTrue(doc.getWriteProtection().isWriteProtected());

 builder = new DocumentBuilder(doc);
 builder.moveToDocumentEnd();
 builder.writeln("Writing text in a protected document.");

 Assert.assertEquals("Hello world! This document is protected." +
         "\rWriting text in a protected document.", doc.getText().trim());
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| contraseña | java.lang.String | La contraseña a establecer. No puede ser  null , pero puede ser una cadena vacía. |

### setReadOnlyRecommended(boolean value) {#setReadOnlyRecommended-boolean}
```
public void setReadOnlyRecommended(boolean value)
```


Especifica si el autor del documento ha recomendado que el documento se abra como solo lectura.

 **Examples:** 

Muestra cómo proteger un documento con una contraseña.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world! This document is protected.");
 // Enter a password up to 15 characters in length, and then verify the document's protection status.
 doc.getWriteProtection().setPassword("MyPassword");
 doc.getWriteProtection().setReadOnlyRecommended(true);

 Assert.assertTrue(doc.getWriteProtection().isWriteProtected());
 Assert.assertTrue(doc.getWriteProtection().validatePassword("MyPassword"));

 // Protection does not prevent the document from being edited programmatically, nor does it encrypt the contents.
 doc.save(getArtifactsDir() + "Document.WriteProtection.docx");
 doc = new Document(getArtifactsDir() + "Document.WriteProtection.docx");

 Assert.assertTrue(doc.getWriteProtection().isWriteProtected());

 builder = new DocumentBuilder(doc);
 builder.moveToDocumentEnd();
 builder.writeln("Writing text in a protected document.");

 Assert.assertEquals("Hello world! This document is protected." +
         "\rWriting text in a protected document.", doc.getText().trim());
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### validatePassword(String password) {#validatePassword-java.lang.String}
```
public boolean validatePassword(String password)
```


Devuelve  true  si la contraseña especificada es la misma que la contraseña de protección contra escritura con la que se protegió el documento. Si el documento no está protegido contra escritura con contraseña, devuelve  false .

 **Examples:** 

Muestra cómo proteger un documento con una contraseña.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world! This document is protected.");
 // Enter a password up to 15 characters in length, and then verify the document's protection status.
 doc.getWriteProtection().setPassword("MyPassword");
 doc.getWriteProtection().setReadOnlyRecommended(true);

 Assert.assertTrue(doc.getWriteProtection().isWriteProtected());
 Assert.assertTrue(doc.getWriteProtection().validatePassword("MyPassword"));

 // Protection does not prevent the document from being edited programmatically, nor does it encrypt the contents.
 doc.save(getArtifactsDir() + "Document.WriteProtection.docx");
 doc = new Document(getArtifactsDir() + "Document.WriteProtection.docx");

 Assert.assertTrue(doc.getWriteProtection().isWriteProtected());

 builder = new DocumentBuilder(doc);
 builder.moveToDocumentEnd();
 builder.writeln("Writing text in a protected document.");

 Assert.assertEquals("Hello world! This document is protected." +
         "\rWriting text in a protected document.", doc.getText().trim());
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| contraseña | java.lang.String |  |

**Returns:**
boolean
