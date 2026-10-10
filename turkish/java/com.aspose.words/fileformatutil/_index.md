---
title: "FileFormatUtil"
linktitle: "FileFormatUtil"
second_title: "Aspose.Words Java için"
description: "Java'da dosya formatını algılamak veya dosya uzantılarını dosya formatı enum'larına/enum'lardan dönüştürmek gibi dosya formatlarıyla çalışmak için yardımcı yöntemler sağlar."
type: docs
weight: 310
url: /tr/java/com.aspose.words/fileformatutil/
---

**Inheritance:**
java.lang.Object
```
public class FileFormatUtil
```

Dosya formatlarıyla çalışmak için yardımcı yöntemler sağlar; örneğin dosya formatını algılamak veya dosya uzantılarını format enum'larına/enum'larından dönüştürmek.

Daha fazla bilgi edinmek için [ Detect File Format and Check Format Compatibility ][Detect File Format and Check Format Compatibility] dokümantasyon makalesini ziyaret edin.

 **Examples:** 

Bir html dosyasındaki kodlamayı nasıl algılayacağınızı gösterir.

```

 FileFormatInfo info = FileFormatUtil.detectFileFormat(getMyDir() + "Document.html");

 Assert.assertEquals(LoadFormat.HTML, info.getLoadFormat());

 // The Encoding property is used only when we create a FileFormatInfo object for an html document.
 Assert.assertEquals("windows-1252", info.getEncoding().name());
 
```


[Detect File Format and Check Format Compatibility]: https://docs.aspose.com/words/java/detect-file-format-and-check-format-compatibility/
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [contentTypeToLoadFormat(String contentType)](#contentTypeToLoadFormat-java.lang.String) | IANA içerik tipini bir yükleme formatı enum değerine dönüştürür. |
| [contentTypeToSaveFormat(String contentType)](#contentTypeToSaveFormat-java.lang.String) | IANA içerik tipini bir kaydetme formatı enum değerine dönüştürür. |
| [detectFileFormat(InputStream stream)](#detectFileFormat-java.io.InputStream) |  |
| [detectFileFormat(String fileName)](#detectFileFormat-java.lang.String) | Bir belgenin formatı hakkında bilgiyi algılar ve döndürür. |
| [extensionToSaveFormat(String extension)](#extensionToSaveFormat-java.lang.String) | Bir dosya adı uzantısını bir [SaveFormat](../../com.aspose.words/saveformat/) değerine dönüştürür. |
| [imageTypeToExtension(int imageType)](#imageTypeToExtension-int) |  |
| [loadFormatToExtension(int loadFormat)](#loadFormatToExtension-int) |  |
| [loadFormatToSaveFormat(int loadFormat)](#loadFormatToSaveFormat-int) |  |
| [saveFormatToExtension(int saveFormat)](#saveFormatToExtension-int) |  |
| [saveFormatToLoadFormat(int saveFormat)](#saveFormatToLoadFormat-int) |  |
### contentTypeToLoadFormat(String contentType) {#contentTypeToLoadFormat-java.lang.String}
```
public static int contentTypeToLoadFormat(String contentType)
```


IANA içerik tipini bir yükleme formatı enum değerine dönüştürür.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| contentType | java.lang.String |  |

**Returns:**
int
### contentTypeToSaveFormat(String contentType) {#contentTypeToSaveFormat-java.lang.String}
```
public static int contentTypeToSaveFormat(String contentType)
```


IANA içerik tipini bir kaydetme formatı enum değerine dönüştürür.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| contentType | java.lang.String |  |

**Returns:**
int
### detectFileFormat(InputStream stream) {#detectFileFormat-java.io.InputStream}
```
public static FileFormatInfo detectFileFormat(InputStream stream)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| stream | java.io.InputStream |  |

**Returns:**
[FileFormatInfo](../../com.aspose.words/fileformatinfo/)
### detectFileFormat(String fileName) {#detectFileFormat-java.lang.String}
```
public static FileFormatInfo detectFileFormat(String fileName)
```


Bir belgenin formatı hakkında bilgiyi algılar ve döndürür.  Diskte depolanan bir belgenin formatı hakkında bilgiyi algılar ve döndürür.

 **Remarks:** 

Bu yöntem belge formatını algılsa bile, belirtilen belgenin geçerli olduğunu garanti etmez. Bu yöntem yalnızca algılamaya yetecek verileri okuyarak belge formatını algılar. Bir belgenin gerçekten geçerli olduğunu tam olarak doğrulamak için belgeyi bir [Document](../../com.aspose.words/document/) nesnesine yüklemeniz gerekir.

Bu yöntem, format tanındığında ancak bozulma nedeniyle algılama tamamlanamadığında [FileCorruptedException](../../com.aspose.words/filecorruptedexception/) fırlatır.

 **Examples:** 

FileFormatUtil sınıfını belge formatını ve şifrelemeyi algılamak için nasıl kullanacağınızı gösterir.

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

FileFormatUtil sınıfını belge formatını ve dijital imzaların varlığını algılamak için nasıl kullanacağınızı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fileName | java.lang.String | Dosya adı. |

**Returns:**
[FileFormatInfo](../../com.aspose.words/fileformatinfo/) - A [FileFormatInfo](../../com.aspose.words/fileformatinfo/) object that contains the detected information.
### extensionToSaveFormat(String extension) {#extensionToSaveFormat-java.lang.String}
```
public static int extensionToSaveFormat(String extension)
```


Bir dosya adı uzantısını bir [SaveFormat](../../com.aspose.words/saveformat/) değerine dönüştürür.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| extension | java.lang.String | Dosya uzantısı. Başında nokta olup olmadan olabilir. Büyük/küçük harfe duyarsız. |

**Returns:**
int
### imageTypeToExtension(int imageType) {#imageTypeToExtension-int}
```
public static String imageTypeToExtension(int imageType)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| imageType | int |  |

**Returns:**
java.lang.String
### loadFormatToExtension(int loadFormat) {#loadFormatToExtension-int}
```
public static String loadFormatToExtension(int loadFormat)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| loadFormat | int |  |

**Returns:**
java.lang.String
### loadFormatToSaveFormat(int loadFormat) {#loadFormatToSaveFormat-int}
```
public static int loadFormatToSaveFormat(int loadFormat)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| loadFormat | int |  |

**Returns:**
int
### saveFormatToExtension(int saveFormat) {#saveFormatToExtension-int}
```
public static String saveFormatToExtension(int saveFormat)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| saveFormat | int |  |

**Returns:**
java.lang.String
### saveFormatToLoadFormat(int saveFormat) {#saveFormatToLoadFormat-int}
```
public static int saveFormatToLoadFormat(int saveFormat)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| saveFormat | int |  |

**Returns:**
int
