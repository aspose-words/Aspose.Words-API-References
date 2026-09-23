---
title: "FileFormatUtil"
linktitle: "FileFormatUtil"
second_title: "Aspose.Words pour Java"
description: "Fournit des méthodes utilitaires pour travailler avec les formats de fichiers, telles que la détection du format de fichier ou la conversion des extensions de fichier vers ou depuis les énumérations de formats de fichier en Java."
type: docs
weight: 310
url: /fr/java/com.aspose.words/fileformatutil/
---

**Inheritance:**
java.lang.Object
```
public class FileFormatUtil
```

Fournit des méthodes utilitaires pour travailler avec les formats de fichiers, comme la détection du format de fichier ou la conversion des extensions de fichiers vers/depuis les énumérations de formats de fichiers.

Pour en savoir plus, consultez l'article de documentation [ Detect File Format and Check Format Compatibility ][Detect File Format and Check Format Compatibility].

 **Examples:** 

Montre comment détecter l'encodage dans un fichier HTML.

```

 FileFormatInfo info = FileFormatUtil.detectFileFormat(getMyDir() + "Document.html");

 Assert.assertEquals(LoadFormat.HTML, info.getLoadFormat());

 // The Encoding property is used only when we create a FileFormatInfo object for an html document.
 Assert.assertEquals("windows-1252", info.getEncoding().name());
 
```


[Detect File Format and Check Format Compatibility]: https://docs.aspose.com/words/java/detect-file-format-and-check-format-compatibility/
## Méthodes

| Méthode | Description |
| --- | --- |
| [contentTypeToLoadFormat(String contentType)](#contentTypeToLoadFormat-java.lang.String) | Convertit le type de contenu IANA en une valeur d'énumération de format de chargement. |
| [contentTypeToSaveFormat(String contentType)](#contentTypeToSaveFormat-java.lang.String) | Convertit le type de contenu IANA en une valeur d'énumération de format d'enregistrement. |
| [detectFileFormat(InputStream stream)](#detectFileFormat-java.io.InputStream) |  |
| [detectFileFormat(String fileName)](#detectFileFormat-java.lang.String) | Détecte et renvoie les informations sur le format d'un document. |
| [extensionToSaveFormat(String extension)](#extensionToSaveFormat-java.lang.String) | Convertit une extension de nom de fichier en une valeur [SaveFormat](../../com.aspose.words/saveformat/). |
| [imageTypeToExtension(int imageType)](#imageTypeToExtension-int) |  |
| [loadFormatToExtension(int loadFormat)](#loadFormatToExtension-int) |  |
| [loadFormatToSaveFormat(int loadFormat)](#loadFormatToSaveFormat-int) |  |
| [saveFormatToExtension(int saveFormat)](#saveFormatToExtension-int) |  |
| [saveFormatToLoadFormat(int saveFormat)](#saveFormatToLoadFormat-int) |  |
### contentTypeToLoadFormat(String contentType) {#contentTypeToLoadFormat-java.lang.String}
```
public static int contentTypeToLoadFormat(String contentType)
```


Convertit le type de contenu IANA en une valeur d'énumération de format de chargement.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| contentType | java.lang.String |  |

**Returns:**
int
### contentTypeToSaveFormat(String contentType) {#contentTypeToSaveFormat-java.lang.String}
```
public static int contentTypeToSaveFormat(String contentType)
```


Convertit le type de contenu IANA en une valeur d'énumération de format d'enregistrement.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| contentType | java.lang.String |  |

**Returns:**
int
### detectFileFormat(InputStream stream) {#detectFileFormat-java.io.InputStream}
```
public static FileFormatInfo detectFileFormat(InputStream stream)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| stream | java.io.InputStream |  |

**Returns:**
[FileFormatInfo](../../com.aspose.words/fileformatinfo/)
### detectFileFormat(String fileName) {#detectFileFormat-java.lang.String}
```
public static FileFormatInfo detectFileFormat(String fileName)
```


Détecte et renvoie les informations sur le format d'un document.  Détecte et renvoie les informations sur le format d'un document stocké dans un fichier disque.

 **Remarks:** 

Même si cette méthode détecte le format du document, elle ne garantit pas que le document spécifié soit valide. Cette méthode ne fait que détecter le format du document en lisant les données suffisantes pour la détection. Pour vérifier pleinement qu'un document est valide, vous devez charger le document dans un objet [Document](../../com.aspose.words/document/).

Cette méthode lève [FileCorruptedException](../../com.aspose.words/filecorruptedexception/) lorsque le format est reconnu, mais que la détection ne peut pas se terminer en raison d'une corruption.

 **Examples:** 

Montre comment utiliser la classe FileFormatUtil pour détecter le format du document et le chiffrement.

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

Montre comment utiliser la classe FileFormatUtil pour détecter le format du document et la présence de signatures numériques.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| fileName | java.lang.String | Le nom du fichier. |

**Returns:**
[FileFormatInfo](../../com.aspose.words/fileformatinfo/) - A [FileFormatInfo](../../com.aspose.words/fileformatinfo/) object that contains the detected information.
### extensionToSaveFormat(String extension) {#extensionToSaveFormat-java.lang.String}
```
public static int extensionToSaveFormat(String extension)
```


Convertit une extension de nom de fichier en une valeur [SaveFormat](../../com.aspose.words/saveformat/).

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| extension | java.lang.String | L'extension du fichier. Peut être avec ou sans point initial. Insensible à la casse. |

**Returns:**
int
### imageTypeToExtension(int imageType) {#imageTypeToExtension-int}
```
public static String imageTypeToExtension(int imageType)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| imageType | int |  |

**Returns:**
java.lang.String
### loadFormatToExtension(int loadFormat) {#loadFormatToExtension-int}
```
public static String loadFormatToExtension(int loadFormat)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| loadFormat | int |  |

**Returns:**
java.lang.String
### loadFormatToSaveFormat(int loadFormat) {#loadFormatToSaveFormat-int}
```
public static int loadFormatToSaveFormat(int loadFormat)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| loadFormat | int |  |

**Returns:**
int
### saveFormatToExtension(int saveFormat) {#saveFormatToExtension-int}
```
public static String saveFormatToExtension(int saveFormat)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| saveFormat | int |  |

**Returns:**
java.lang.String
### saveFormatToLoadFormat(int saveFormat) {#saveFormatToLoadFormat-int}
```
public static int saveFormatToLoadFormat(int saveFormat)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| saveFormat | int |  |

**Returns:**
int
