---
title: "FileFormatInfo"
linktitle: "FileFormatInfo"
second_title: "Aspose.Words Java için"
description: "Java'da FileFormatUtil belge formatı algılama yöntemleri tarafından döndürülen verileri içerir."
type: docs
weight: 309
url: /tr/java/com.aspose.words/fileformatinfo/
---

**Inheritance:**
java.lang.Object
```
public class FileFormatInfo
```

[FileFormatUtil](../../com.aspose.words/fileformatutil/) belge formatı algılama yöntemleri tarafından döndürülen verileri içerir.

Daha fazla bilgi edinmek için [ Detect File Format and Check Format Compatibility ][Detect File Format and Check Format Compatibility] dokümantasyon makalesini ziyaret edin.

 **Remarks:** 

Bu sınıfın örneklerini doğrudan oluşturmazsınız. Bu sınıfın nesneleri **M:Aspose.Words.FileFormatUtil.DetectFileFormat(System.IO.Stream)** yöntemleri tarafından döndürülür.

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


[Detect File Format and Check Format Compatibility]: https://docs.aspose.com/words/java/detect-file-format-and-check-format-compatibility/
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getEncoding()](#getEncoding) | Mevcut belge formatına uygulanabiliyorsa algılanan kodlamayı alır. |
| [getLoadFormat()](#getLoadFormat) | Algılanan belge formatını alır. |
| [hasDigitalSignature()](#hasDigitalSignature) | Bu belge bir dijital imza içeriyorsa  true  değerini döndürür. |
| [hasMacros()](#hasMacros) | Bu belge bir VBA makrosu içeriyorsa  true  değerini döndürür. |
| [isEncrypted()](#isEncrypted) | Belge şifrelenmiş ve açmak için bir parola gerekiyorsa  true  değerini döndürür. |
### getEncoding() {#getEncoding}
```
public Charset getEncoding()
```


Mevcut belge formatına uygulanabiliyorsa algılanan kodlamayı alır. Şu anda yalnızca HTML belgeleri için kodlamayı algılar.

 **Examples:** 

Bir html dosyasındaki kodlamayı nasıl algılayacağınızı gösterir.

```

 FileFormatInfo info = FileFormatUtil.detectFileFormat(getMyDir() + "Document.html");

 Assert.assertEquals(LoadFormat.HTML, info.getLoadFormat());

 // The Encoding property is used only when we create a FileFormatInfo object for an html document.
 Assert.assertEquals("windows-1252", info.getEncoding().name());
 
```

**Returns:**
java.nio.charset.Charset - Mevcut belge formatına uygulanabiliyorsa algılanan kodlama.
### getLoadFormat() {#getLoadFormat}
```
public int getLoadFormat()
```


Algılanan belge formatını alır.

 **Remarks:** 

Bir OOXML belgesi şifrelenmiş olduğunda, önce şifresi çözülmeden bunun Excel, Word ya da PowerPoint belgesi olup olduğu belirlenemez; bu nedenle şifreli bir OOXML belgesi için bu özellik her zaman [LoadFormat.DOCX](../../com.aspose.words/loadformat/\#DOCX) değerini döndürür.

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

Bir belgenin formatını tespit etmek için FileFormatUtil yöntemlerinin nasıl kullanılacağını gösterir.

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
int - Algılanan belge formatı. Döndürülen değer, [LoadFormat](../../com.aspose.words/loadformat/) sabitlerinden biridir.
### hasDigitalSignature() {#hasDigitalSignature}
```
public boolean hasDigitalSignature()
```


Bu belge bir dijital imza içeriyorsa  true  değerini döndürür. Bu özellik yalnızca bir dijital imzanın belgede bulunduğunu bildirir, ancak imzanın geçerli olup olmadığını belirtmez.

 **Remarks:** 

Bu özellik, dijital olarak imzalanmış belgeleri imzası olmayanlardan ayırmanıza yardımcı olmak için vardır. Aspose.Words kullanarak dijital olarak imzalanmış bir belgeyi değiştirir ve kaydederseniz, dijital imza kaybolur. Bu, bir dijital imzanın belgenin özgünlüğünü korumak için var olduğu tasarım gereğidir. Bu özelliği kullanarak, normal belgeler gibi işleme almadan önce dijital imzalı belgeleri tespit edebilir ve dijital imzanın kaybolmasını önlemek için, örneğin kullanıcıyı bilgilendirmek gibi bir eylemde bulunabilirsiniz.

 **Examples:** 

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

**Returns:**
boolean -  true  bu belge bir dijital imza içeriyorsa.
### hasMacros() {#hasMacros}
```
public boolean hasMacros()
```


Bu belge bir VBA makrosu içeriyorsa  true  değerini döndürür.

 **Examples:** 

Belgeyi yüklemeden VBA makro varlığını nasıl kontrol edeceğinizi gösterir.

```

 FileFormatInfo fileFormatInfo = FileFormatUtil.detectFileFormat(getMyDir() + "Macro.docm");
 Assert.assertTrue(fileFormatInfo.hasMacros());
 
```

**Returns:**
boolean -  true  bu belge bir VBA makrosu içeriyorsa.
### isEncrypted() {#isEncrypted}
```
public boolean isEncrypted()
```


Belge şifrelenmiş ve açmak için bir parola gerekiyorsa  true  değerini döndürür.

 **Remarks:** 

Bu özellik, şifrelenmiş belgeleri şifrelenmemişlerden ayırmanıza yardımcı olmak için vardır. Aspose.Words kullanarak bir şifreli belgeyi parola sağlamadan yüklemeye çalışırsanız bir istisna fırlatılır. Bu özelliği, bir belgenin parola gerektirip gerektirmediğini tespit etmek ve belgeyi yüklemeden önce bir eylemde bulunmak için kullanabilirsiniz; örneğin kullanıcıdan parola istemek.

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

**Returns:**
boolean -  true  belge şifrelenmiş ve açmak için bir parola gerekiyorsa.
