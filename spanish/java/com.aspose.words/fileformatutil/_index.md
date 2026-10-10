---
title: "FileFormatUtil"
linktitle: "FileFormatUtil"
second_title: "Aspose.Words para Java"
description: "Proporciona métodos utilitarios para trabajar con formatos de archivo, como detectar el formato de archivo o convertir extensiones de archivo a/de enumeraciones de formatos de archivo en Java."
type: docs
weight: 310
url: /es/java/com.aspose.words/fileformatutil/
---

**Inheritance:**
java.lang.Object
```
public class FileFormatUtil
```

Proporciona métodos utilitarios para trabajar con formatos de archivo, como detectar el formato de archivo o convertir extensiones de archivo a/de enumeraciones de formatos de archivo.

Para obtener más información, visite el artículo de documentación [ Detect File Format and Check Format Compatibility ][Detect File Format and Check Format Compatibility].

 **Examples:** 

Muestra cómo detectar la codificación en un archivo HTML.

```

 FileFormatInfo info = FileFormatUtil.detectFileFormat(getMyDir() + "Document.html");

 Assert.assertEquals(LoadFormat.HTML, info.getLoadFormat());

 // The Encoding property is used only when we create a FileFormatInfo object for an html document.
 Assert.assertEquals("windows-1252", info.getEncoding().name());
 
```


[Detect File Format and Check Format Compatibility]: https://docs.aspose.com/words/java/detect-file-format-and-check-format-compatibility/
## Métodos

| Método | Descripción |
| --- | --- |
| [contentTypeToLoadFormat(String contentType)](#contentTypeToLoadFormat-java.lang.String) | Convierte el tipo de contenido IANA en un valor enumerado de formato de carga. |
| [contentTypeToSaveFormat(String contentType)](#contentTypeToSaveFormat-java.lang.String) | Convierte el tipo de contenido IANA en un valor enumerado de formato de guardado. |
| [detectFileFormat(InputStream stream)](#detectFileFormat-java.io.InputStream) |  |
| [detectFileFormat(String fileName)](#detectFileFormat-java.lang.String) | Detecta y devuelve la información sobre el formato de un documento. |
| [extensionToSaveFormat(String extension)](#extensionToSaveFormat-java.lang.String) | Convierte una extensión de nombre de archivo en un valor [SaveFormat](../../com.aspose.words/saveformat/). |
| [imageTypeToExtension(int imageType)](#imageTypeToExtension-int) |  |
| [loadFormatToExtension(int loadFormat)](#loadFormatToExtension-int) |  |
| [loadFormatToSaveFormat(int loadFormat)](#loadFormatToSaveFormat-int) |  |
| [saveFormatToExtension(int saveFormat)](#saveFormatToExtension-int) |  |
| [saveFormatToLoadFormat(int saveFormat)](#saveFormatToLoadFormat-int) |  |
### contentTypeToLoadFormat(String contentType) {#contentTypeToLoadFormat-java.lang.String}
```
public static int contentTypeToLoadFormat(String contentType)
```


Convierte el tipo de contenido IANA en un valor enumerado de formato de carga.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| contentType | java.lang.String |  |

**Returns:**
int
### contentTypeToSaveFormat(String contentType) {#contentTypeToSaveFormat-java.lang.String}
```
public static int contentTypeToSaveFormat(String contentType)
```


Convierte el tipo de contenido IANA en un valor enumerado de formato de guardado.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| contentType | java.lang.String |  |

**Returns:**
int
### detectFileFormat(InputStream stream) {#detectFileFormat-java.io.InputStream}
```
public static FileFormatInfo detectFileFormat(InputStream stream)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| stream | java.io.InputStream |  |

**Returns:**
[FileFormatInfo](../../com.aspose.words/fileformatinfo/)
### detectFileFormat(String fileName) {#detectFileFormat-java.lang.String}
```
public static FileFormatInfo detectFileFormat(String fileName)
```


Detecta y devuelve la información sobre el formato de un documento.  Detecta y devuelve la información sobre el formato de un documento almacenado en un archivo de disco.

 **Remarks:** 

Aunque este método detecte el formato del documento, no garantiza que el documento especificado sea válido. Este método solo detecta el formato del documento leyendo datos suficientes para la detección. Para verificar completamente que un documento es válido, debe cargar el documento en un objeto [Document](../../com.aspose.words/document/).

Este método lanza [FileCorruptedException](../../com.aspose.words/filecorruptedexception/) cuando el formato es reconocido, pero la detección no puede completarse debido a corrupción.

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

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fileName | java.lang.String | El nombre del archivo. |

**Returns:**
[FileFormatInfo](../../com.aspose.words/fileformatinfo/) - A [FileFormatInfo](../../com.aspose.words/fileformatinfo/) object that contains the detected information.
### extensionToSaveFormat(String extension) {#extensionToSaveFormat-java.lang.String}
```
public static int extensionToSaveFormat(String extension)
```


Convierte una extensión de nombre de archivo en un valor [SaveFormat](../../com.aspose.words/saveformat/).

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| extension | java.lang.String | La extensión del archivo. Puede ser con o sin un punto inicial. No distingue entre mayúsculas y minúsculas. |

**Returns:**
int
### imageTypeToExtension(int imageType) {#imageTypeToExtension-int}
```
public static String imageTypeToExtension(int imageType)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| imageType | int |  |

**Returns:**
java.lang.String
### loadFormatToExtension(int loadFormat) {#loadFormatToExtension-int}
```
public static String loadFormatToExtension(int loadFormat)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| loadFormat | int |  |

**Returns:**
java.lang.String
### loadFormatToSaveFormat(int loadFormat) {#loadFormatToSaveFormat-int}
```
public static int loadFormatToSaveFormat(int loadFormat)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| loadFormat | int |  |

**Returns:**
int
### saveFormatToExtension(int saveFormat) {#saveFormatToExtension-int}
```
public static String saveFormatToExtension(int saveFormat)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| saveFormat | int |  |

**Returns:**
java.lang.String
### saveFormatToLoadFormat(int saveFormat) {#saveFormatToLoadFormat-int}
```
public static int saveFormatToLoadFormat(int saveFormat)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| saveFormat | int |  |

**Returns:**
int
