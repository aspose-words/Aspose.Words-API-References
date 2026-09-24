---
title: "FileFormatInfo"
linktitle: "FileFormatInfo"
second_title: "Aspose.Words para Java"
description: "Contiene datos devueltos por los métodos de detección de formato de documento de FileFormatUtil en Java."
type: docs
weight: 309
url: /es/java/com.aspose.words/fileformatinfo/
---

**Inheritance:**
java.lang.Object
```
public class FileFormatInfo
```

Contiene datos devueltos por los métodos de detección de formato de documento de [FileFormatUtil](../../com.aspose.words/fileformatutil/).

Para obtener más información, visite el artículo de documentación [ Detect File Format and Check Format Compatibility ][Detect File Format and Check Format Compatibility].

 **Remarks:** 

No crea instancias de esta clase directamente. Los objetos de esta clase son devueltos por los métodos **M:Aspose.Words.FileFormatUtil.DetectFileFormat(System.IO.Stream)**.

 **Examples:** 

Muestra cómo usar la clase FileFormatUtil para detectar el formato del documento y el cifrado.

```

 Document doc = new Document();

 // Configure a SaveOptions object to encrypt the document
 // with a password when we save it, and then save the document.
 OdtSaveOptions saveOptions = new OdtSaveOptions(SaveFormat.ODT);
 saveOptions.setPassword("MyPassword");

 doc.save(getArtifactsDir() + "File.DetectDocumentEncryption.odt", saveOptions);

 // Verify the file type of our document, and its encryption status.
 FileFormatInfo info = FileFormatUtil.detectFileFormat(getArtifactsDir() + "File.DetectDocumentEncryption.odt");

 Assert.assertEquals(".odt", FileFormatUtil.loadFormatToExtension(info.getLoadFormat()));
 Assert.assertTrue(info.isEncrypted());
 
```

Muestra cómo usar la clase FileFormatUtil para detectar el formato del documento y la presencia de firmas digitales.

```

 // Use a FileFormatInfo instance to verify that a document is not digitally signed.
 FileFormatInfo info = FileFormatUtil.detectFileFormat(getMyDir() + "Document.docx");

 Assert.assertEquals(".docx", FileFormatUtil.loadFormatToExtension(info.getLoadFormat()));
 Assert.assertFalse(info.hasDigitalSignature());

 CertificateHolder certificateHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw", null);
 DigitalSignatureUtil.sign(getMyDir() + "Document.docx", getArtifactsDir() + "File.DetectDigitalSignatures.docx",
         certificateHolder);

 // Use a new FileFormatInstance to confirm that it is signed.
 info = FileFormatUtil.detectFileFormat(getArtifactsDir() + "File.DetectDigitalSignatures.docx");

 Assert.assertTrue(info.hasDigitalSignature());

 // We can load and access the signatures of a signed document in a collection like this.
 Assert.assertEquals(1, DigitalSignatureUtil.loadSignatures(getArtifactsDir() + "File.DetectDigitalSignatures.docx").getCount());
 
```


[Detect File Format and Check Format Compatibility]: https://docs.aspose.com/words/java/detect-file-format-and-check-format-compatibility/
## Métodos

| Método | Descripción |
| --- | --- |
| [getEncoding()](#getEncoding) | Obtiene la codificación detectada si es aplicable al formato de documento actual. |
| [getLoadFormat()](#getLoadFormat) | Obtiene el formato de documento detectado. |
| [hasDigitalSignature()](#hasDigitalSignature) | Devuelve  true  si este documento contiene una firma digital. |
| [hasMacros()](#hasMacros) | Devuelve  true  si este documento contiene macros VBA. |
| [isEncrypted()](#isEncrypted) | Devuelve  true  si el documento está encriptado y requiere una contraseña para abrirse. |
### getEncoding() {#getEncoding}
```
public Charset getEncoding()
```


Obtiene la codificación detectada si es aplicable al formato de documento actual. En este momento solo detecta la codificación para documentos HTML.

 **Examples:** 

Muestra cómo detectar la codificación en un archivo HTML.

```

 FileFormatInfo info = FileFormatUtil.detectFileFormat(getMyDir() + "Document.html");

 Assert.assertEquals(LoadFormat.HTML, info.getLoadFormat());

 // The Encoding property is used only when we create a FileFormatInfo object for an html document.
 Assert.assertEquals("windows-1252", info.getEncoding().name());
 
```

**Returns:**
java.nio.charset.Charset - La codificación detectada si es aplicable al formato de documento actual.
### getLoadFormat() {#getLoadFormat}
```
public int getLoadFormat()
```


Obtiene el formato de documento detectado.

 **Remarks:** 

Cuando un documento OOXML está encriptado, no es posible determinar si es un documento de Excel, Word o PowerPoint sin descifrarlo primero, por lo que para un documento OOXML encriptado esta propiedad siempre devolverá [LoadFormat.DOCX](../../com.aspose.words/loadformat/\#DOCX).

 **Examples:** 

Muestra cómo usar la clase FileFormatUtil para detectar el formato del documento y el cifrado.

```

 Document doc = new Document();

 // Configure a SaveOptions object to encrypt the document
 // with a password when we save it, and then save the document.
 OdtSaveOptions saveOptions = new OdtSaveOptions(SaveFormat.ODT);
 saveOptions.setPassword("MyPassword");

 doc.save(getArtifactsDir() + "File.DetectDocumentEncryption.odt", saveOptions);

 // Verify the file type of our document, and its encryption status.
 FileFormatInfo info = FileFormatUtil.detectFileFormat(getArtifactsDir() + "File.DetectDocumentEncryption.odt");

 Assert.assertEquals(".odt", FileFormatUtil.loadFormatToExtension(info.getLoadFormat()));
 Assert.assertTrue(info.isEncrypted());
 
```

Muestra cómo usar la clase FileFormatUtil para detectar el formato del documento y la presencia de firmas digitales.

```

 // Use a FileFormatInfo instance to verify that a document is not digitally signed.
 FileFormatInfo info = FileFormatUtil.detectFileFormat(getMyDir() + "Document.docx");

 Assert.assertEquals(".docx", FileFormatUtil.loadFormatToExtension(info.getLoadFormat()));
 Assert.assertFalse(info.hasDigitalSignature());

 CertificateHolder certificateHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw", null);
 DigitalSignatureUtil.sign(getMyDir() + "Document.docx", getArtifactsDir() + "File.DetectDigitalSignatures.docx",
         certificateHolder);

 // Use a new FileFormatInstance to confirm that it is signed.
 info = FileFormatUtil.detectFileFormat(getArtifactsDir() + "File.DetectDigitalSignatures.docx");

 Assert.assertTrue(info.hasDigitalSignature());

 // We can load and access the signatures of a signed document in a collection like this.
 Assert.assertEquals(1, DigitalSignatureUtil.loadSignatures(getArtifactsDir() + "File.DetectDigitalSignatures.docx").getCount());
 
```

Muestra cómo usar los métodos de FileFormatUtil para detectar el formato de un documento.

```

 // Load a document from a file that is missing a file extension, and then detect its file format.
 FileInputStream docStream = new FileInputStream(getMyDir() + "Word document with missing file extension");

 FileFormatInfo info = FileFormatUtil.detectFileFormat(docStream);

 int loadFormat = info.getLoadFormat();

 Assert.assertEquals(LoadFormat.DOC, loadFormat);

 // Below are two methods of converting a LoadFormat to its corresponding SaveFormat.
 // 1 -  Get the file extension string for the LoadFormat, then get the corresponding SaveFormat from that string:
 String fileExtension = FileFormatUtil.loadFormatToExtension(loadFormat);

 int saveFormat = FileFormatUtil.extensionToSaveFormat(fileExtension);

 // 2 -  Convert the LoadFormat directly to its SaveFormat:
 saveFormat = FileFormatUtil.loadFormatToSaveFormat(loadFormat);

 // Load a document from the stream, and then save it to the automatically detected file extension.
 Document doc = new Document(docStream);

 Assert.assertEquals(".doc", FileFormatUtil.saveFormatToExtension(saveFormat));

 doc.save(getArtifactsDir() + "File.SaveToDetectedFileFormat" + FileFormatUtil.saveFormatToExtension(saveFormat));
 
```

**Returns:**
int - El formato de documento detectado. El valor devuelto es una de las constantes de [LoadFormat](../../com.aspose.words/loadformat/).
### hasDigitalSignature() {#hasDigitalSignature}
```
public boolean hasDigitalSignature()
```


Devuelve  true  si este documento contiene una firma digital. Esta propiedad simplemente indica que una firma digital está presente en un documento, pero no especifica si la firma es válida o no.

 **Remarks:** 

Esta propiedad existe para ayudarle a ordenar los documentos que están firmados digitalmente de los que no lo están. Si utiliza Aspose.Words para modificar y guardar un documento que está firmado digitalmente, la firma digital se perderá. Esto es intencional porque una firma digital existe para proteger la autenticidad de un documento. Usando esta propiedad puede detectar documentos firmados digitalmente antes de procesarlos de la misma manera que los documentos normales y tomar alguna acción para evitar perder la firma digital, por ejemplo notificar al usuario.

 **Examples:** 

Muestra cómo usar la clase FileFormatUtil para detectar el formato del documento y la presencia de firmas digitales.

```

 // Use a FileFormatInfo instance to verify that a document is not digitally signed.
 FileFormatInfo info = FileFormatUtil.detectFileFormat(getMyDir() + "Document.docx");

 Assert.assertEquals(".docx", FileFormatUtil.loadFormatToExtension(info.getLoadFormat()));
 Assert.assertFalse(info.hasDigitalSignature());

 CertificateHolder certificateHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw", null);
 DigitalSignatureUtil.sign(getMyDir() + "Document.docx", getArtifactsDir() + "File.DetectDigitalSignatures.docx",
         certificateHolder);

 // Use a new FileFormatInstance to confirm that it is signed.
 info = FileFormatUtil.detectFileFormat(getArtifactsDir() + "File.DetectDigitalSignatures.docx");

 Assert.assertTrue(info.hasDigitalSignature());

 // We can load and access the signatures of a signed document in a collection like this.
 Assert.assertEquals(1, DigitalSignatureUtil.loadSignatures(getArtifactsDir() + "File.DetectDigitalSignatures.docx").getCount());
 
```

**Returns:**
boolean -  true  si este documento contiene una firma digital.
### hasMacros() {#hasMacros}
```
public boolean hasMacros()
```


Devuelve  true  si este documento contiene macros VBA.

 **Examples:** 

Muestra cómo comprobar la presencia de macros VBA sin cargar el documento.

```

 FileFormatInfo fileFormatInfo = FileFormatUtil.detectFileFormat(getMyDir() + "Macro.docm");
 Assert.assertTrue(fileFormatInfo.hasMacros());
 
```

**Returns:**
boolean -  true  si este documento contiene macros VBA.
### isEncrypted() {#isEncrypted}
```
public boolean isEncrypted()
```


Devuelve  true  si el documento está encriptado y requiere una contraseña para abrirse.

 **Remarks:** 

Esta propiedad existe para ayudarle a ordenar los documentos que están encriptados de los que no lo están. Si intenta cargar un documento encriptado usando Aspose.Words sin proporcionar una contraseña, se lanzará una excepción. Puede usar esta propiedad para detectar si un documento requiere una contraseña y tomar alguna acción antes de cargar el documento, por ejemplo, solicitar al usuario una contraseña.

 **Examples:** 

Muestra cómo usar la clase FileFormatUtil para detectar el formato del documento y el cifrado.

```

 Document doc = new Document();

 // Configure a SaveOptions object to encrypt the document
 // with a password when we save it, and then save the document.
 OdtSaveOptions saveOptions = new OdtSaveOptions(SaveFormat.ODT);
 saveOptions.setPassword("MyPassword");

 doc.save(getArtifactsDir() + "File.DetectDocumentEncryption.odt", saveOptions);

 // Verify the file type of our document, and its encryption status.
 FileFormatInfo info = FileFormatUtil.detectFileFormat(getArtifactsDir() + "File.DetectDocumentEncryption.odt");

 Assert.assertEquals(".odt", FileFormatUtil.loadFormatToExtension(info.getLoadFormat()));
 Assert.assertTrue(info.isEncrypted());
 
```

**Returns:**
boolean -  true  si el documento está encriptado y requiere una contraseña para abrirse.
