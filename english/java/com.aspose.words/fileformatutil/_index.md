---
title: FileFormatUtil
linktitle: FileFormatUtil
second_title: Aspose.Words for Java
description: Provides utility methods for working with file formats such as detecting file format or converting file extensions to/from file format enums in Java.
type: docs
weight: 300
url: /java/com.aspose.words/fileformatutil/
---

**Inheritance:**
java.lang.Object
```
public class FileFormatUtil
```

Provides utility methods for working with file formats, such as detecting file format or converting file extensions to/from file format enums.

To learn more, visit the [ Detect File Format and Check Format Compatibility ][Detect File Format and Check Format Compatibility] documentation article.

 **Examples:** 

Shows how to detect encoding in an html file.

```

 FileFormatInfo info = FileFormatUtil.detectFileFormat(getMyDir() + "Document.html");

 Assert.assertEquals(LoadFormat.HTML, info.getLoadFormat());

 // The Encoding property is used only when we create a FileFormatInfo object for an html document.
 Assert.assertEquals("windows-1252", info.getEncoding().name());
 
```


[Detect File Format and Check Format Compatibility]: https://docs.aspose.com/words/java/detect-file-format-and-check-format-compatibility/
## Methods

| Method | Description |
| --- | --- |
| [contentTypeToLoadFormat(String contentType)](#contentTypeToLoadFormat-java.lang.String) | Converts IANA content type into a load format enumerated value. |
| [contentTypeToSaveFormat(String contentType)](#contentTypeToSaveFormat-java.lang.String) | Converts IANA content type into a save format enumerated value. |
| [detectFileFormat(InputStream stream)](#detectFileFormat-java.io.InputStream) |  |
| [detectFileFormat(String fileName)](#detectFileFormat-java.lang.String) | Detects and returns the information about a format of a document. |
| [extensionToSaveFormat(String extension)](#extensionToSaveFormat-java.lang.String) | Converts a file name extension into a [SaveFormat](../../com.aspose.words/saveformat/) value. |
| [imageTypeToExtension(int imageType)](#imageTypeToExtension-int) |  |
| [loadFormatToExtension(int loadFormat)](#loadFormatToExtension-int) |  |
| [loadFormatToSaveFormat(int loadFormat)](#loadFormatToSaveFormat-int) |  |
| [saveFormatToExtension(int saveFormat)](#saveFormatToExtension-int) |  |
| [saveFormatToLoadFormat(int saveFormat)](#saveFormatToLoadFormat-int) |  |
### contentTypeToLoadFormat(String contentType) {#contentTypeToLoadFormat-java.lang.String}
```
public static int contentTypeToLoadFormat(String contentType)
```


Converts IANA content type into a load format enumerated value.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| contentType | java.lang.String |  |

**Returns:**
int
### contentTypeToSaveFormat(String contentType) {#contentTypeToSaveFormat-java.lang.String}
```
public static int contentTypeToSaveFormat(String contentType)
```


Converts IANA content type into a save format enumerated value.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| contentType | java.lang.String |  |

**Returns:**
int
### detectFileFormat(InputStream stream) {#detectFileFormat-java.io.InputStream}
```
public static FileFormatInfo detectFileFormat(InputStream stream)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| stream | java.io.InputStream |  |

**Returns:**
[FileFormatInfo](../../com.aspose.words/fileformatinfo/)
### detectFileFormat(String fileName) {#detectFileFormat-java.lang.String}
```
public static FileFormatInfo detectFileFormat(String fileName)
```


Detects and returns the information about a format of a document.  Detects and returns the information about a format of a document stored in a disk file.

 **Remarks:** 

Even if this method detects the document format, it does not guarantee that the specified document is valid. This method only detects the document format by reading data that is sufficient for detection. To fully verify that a document is valid you need to load the document into a [Document](../../com.aspose.words/document/) object.

This method throws [FileCorruptedException](../../com.aspose.words/filecorruptedexception/) when the format is recognized, but the detection cannot complete because of corruption.

 **Examples:** 

Shows how to use the FileFormatUtil class to detect the document format and encryption.

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

Shows how to use the FileFormatUtil class to detect the document format and presence of digital signatures.

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
| Parameter | Type | Description |
| --- | --- | --- |
| fileName | java.lang.String | The file name. |

**Returns:**
[FileFormatInfo](../../com.aspose.words/fileformatinfo/) - A [FileFormatInfo](../../com.aspose.words/fileformatinfo/) object that contains the detected information.
### extensionToSaveFormat(String extension) {#extensionToSaveFormat-java.lang.String}
```
public static int extensionToSaveFormat(String extension)
```


Converts a file name extension into a [SaveFormat](../../com.aspose.words/saveformat/) value.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| extension | java.lang.String | The file extension. Can be with or without a leading dot. Case-insensitive. |

**Returns:**
int
### imageTypeToExtension(int imageType) {#imageTypeToExtension-int}
```
public static String imageTypeToExtension(int imageType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| imageType | int |  |

**Returns:**
java.lang.String
### loadFormatToExtension(int loadFormat) {#loadFormatToExtension-int}
```
public static String loadFormatToExtension(int loadFormat)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| loadFormat | int |  |

**Returns:**
java.lang.String
### loadFormatToSaveFormat(int loadFormat) {#loadFormatToSaveFormat-int}
```
public static int loadFormatToSaveFormat(int loadFormat)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| loadFormat | int |  |

**Returns:**
int
### saveFormatToExtension(int saveFormat) {#saveFormatToExtension-int}
```
public static String saveFormatToExtension(int saveFormat)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| saveFormat | int |  |

**Returns:**
java.lang.String
### saveFormatToLoadFormat(int saveFormat) {#saveFormatToLoadFormat-int}
```
public static int saveFormatToLoadFormat(int saveFormat)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| saveFormat | int |  |

**Returns:**
int
