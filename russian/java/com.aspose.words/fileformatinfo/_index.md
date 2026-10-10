---
title: "FileFormatInfo"
linktitle: "FileFormatInfo"
second_title: "Aspose.Words для Java"
description: "Содержит данные, возвращаемые методами обнаружения формата документа FileFormatUtil в Java."
type: docs
weight: 309
url: /ru/java/com.aspose.words/fileformatinfo/
---

**Inheritance:**
java.lang.Object
```
public class FileFormatInfo
```

Содержит данные, возвращаемые методами обнаружения формата документа [FileFormatUtil](../../com.aspose.words/fileformatutil/).

Чтобы узнать больше, посетите статью документации [ Detect File Format and Check Format Compatibility ][Detect File Format and Check Format Compatibility].

 **Remarks:** 

Вы не создаёте экземпляры этого класса напрямую. Объекты этого класса возвращаются методами **M:Aspose.Words.FileFormatUtil.DetectFileFormat(System.IO.Stream)**.

 **Examples:** 

Показывает, как использовать класс FileFormatUtil для определения формата документа и шифрования.

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

Показывает, как использовать класс FileFormatUtil для определения формата документа и наличия цифровых подписей.

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
## Методы

| Метод | Описание |
| --- | --- |
| [getEncoding()](#getEncoding) | Получает обнаруженную кодировку, если она применима к текущему формату документа. |
| [getLoadFormat()](#getLoadFormat) | Получает обнаруженный формат документа. |
| [hasDigitalSignature()](#hasDigitalSignature) | Возвращает  true  если этот документ содержит цифровую подпись. |
| [hasMacros()](#hasMacros) | Возвращает  true  если этот документ содержит макросы VBA. |
| [isEncrypted()](#isEncrypted) | Возвращает  true  если документ зашифрован и требует пароль для открытия. |
### getEncoding() {#getEncoding}
```
public Charset getEncoding()
```


Получает обнаруженную кодировку, если она применима к текущему формату документа. В данный момент кодировка определяется только для HTML‑документов.

 **Examples:** 

Показывает, как определить кодировку в HTML‑файле.

```

 FileFormatInfo info = FileFormatUtil.detectFileFormat(getMyDir() + "Document.html");

 Assert.assertEquals(LoadFormat.HTML, info.getLoadFormat());

 // The Encoding property is used only when we create a FileFormatInfo object for an html document.
 Assert.assertEquals("windows-1252", info.getEncoding().name());
 
```

**Returns:**
java.nio.charset.Charset - Обнаруженная кодировка, если она применима к текущему формату документа.
### getLoadFormat() {#getLoadFormat}
```
public int getLoadFormat()
```


Получает обнаруженный формат документа.

 **Remarks:** 

Когда OOXML‑документ зашифрован, невозможно определить, является ли он документом Excel, Word или PowerPoint без предварительного расшифрования, поэтому для зашифрованного OOXML‑документа это свойство всегда будет возвращать [LoadFormat.DOCX](../../com.aspose.words/loadformat/\#DOCX).

 **Examples:** 

Показывает, как использовать класс FileFormatUtil для определения формата документа и шифрования.

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

Показывает, как использовать класс FileFormatUtil для определения формата документа и наличия цифровых подписей.

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

Показывает, как использовать методы FileFormatUtil для определения формата документа.

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
int - обнаруженный формат документа. Возвращаемое значение является одной из констант [LoadFormat](../../com.aspose.words/loadformat/).
### hasDigitalSignature() {#hasDigitalSignature}
```
public boolean hasDigitalSignature()
```


Возвращает  true  если этот документ содержит цифровую подпись. Это свойство лишь сообщает, что цифровая подпись присутствует в документе, но не указывает, действительна она или нет.

 **Remarks:** 

Это свойство существует, чтобы помочь вам сортировать документы, подписанные цифровой подписью, от неподписанных. Если вы используете Aspose.Words для изменения и сохранения документа, подписанного цифровой подписью, цифровая подпись будет потеряна. Это сделано намеренно, поскольку цифровая подпись предназначена для защиты подлинности документа. С помощью этого свойства вы можете обнаружить цифрово подписанные документы перед их обработкой так же, как обычные документы, и предпринять некоторые действия, чтобы избежать потери цифровой подписи, например, уведомить пользователя.

 **Examples:** 

Показывает, как использовать класс FileFormatUtil для определения формата документа и наличия цифровых подписей.

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
boolean -  true  если этот документ содержит цифровую подпись.
### hasMacros() {#hasMacros}
```
public boolean hasMacros()
```


Возвращает  true  если этот документ содержит макросы VBA.

 **Examples:** 

Показывает, как проверить наличие макросов VBA без загрузки документа.

```

 FileFormatInfo fileFormatInfo = FileFormatUtil.detectFileFormat(getMyDir() + "Macro.docm");
 Assert.assertTrue(fileFormatInfo.hasMacros());
 
```

**Returns:**
boolean -  true  если этот документ содержит макросы VBA.
### isEncrypted() {#isEncrypted}
```
public boolean isEncrypted()
```


Возвращает  true  если документ зашифрован и требует пароль для открытия.

 **Remarks:** 

Это свойство существует, чтобы помочь вам сортировать документы, зашифрованные, от незашифрованных. Если вы попытаетесь загрузить зашифрованный документ с помощью Aspose.Words без указания пароля, будет выброшено исключение. Вы можете использовать это свойство, чтобы определить, требуется ли документу пароль, и выполнить некоторые действия до загрузки документа, например, запросить пароль у пользователя.

 **Examples:** 

Показывает, как использовать класс FileFormatUtil для определения формата документа и шифрования.

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
boolean -  true  если документ зашифрован и требует пароль для открытия.
