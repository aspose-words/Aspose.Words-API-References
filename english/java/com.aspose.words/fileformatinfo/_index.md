---
title: FileFormatInfo
linktitle: FileFormatInfo
second_title: Aspose.Words for Java
description: Contains data returned by FileFormatUtil document format detection methods in Java.
type: docs
weight: 292
url: /java/com.aspose.words/fileformatinfo/
---

**Inheritance:**
java.lang.Object
```
public class FileFormatInfo
```

Contains data returned by [FileFormatUtil](../../com.aspose.words/fileformatutil/) document format detection methods.

To learn more, visit the [ Detect File Format and Check Format Compatibility ][Detect File Format and Check Format Compatibility] documentation article.

 **Remarks:** 

You do not create instances of this class directly. Objects of this class are returned by **M:Aspose.Words.FileFormatUtil.DetectFileFormat(System.IO.Stream)** methods.

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


[Detect File Format and Check Format Compatibility]: https://docs.aspose.com/words/java/detect-file-format-and-check-format-compatibility/
## Methods

| Method | Description |
| --- | --- |
| [getEncoding()](#getEncoding) | Gets the detected encoding if applicable to the current document format. |
| [getLoadFormat()](#getLoadFormat) | Gets the detected document format. |
| [hasDigitalSignature()](#hasDigitalSignature) | Returns  true  if this document contains a digital signature. |
| [hasMacros()](#hasMacros) | Returns  true  if this document contains a VBA macros. |
| [isEncrypted()](#isEncrypted) | Returns  true  if the document is encrypted and requires a password to open. |
### getEncoding() {#getEncoding}
```
public Charset getEncoding()
```


Gets the detected encoding if applicable to the current document format. At the moment detects encoding only for HTML documents.

 **Examples:** 

Shows how to detect encoding in an html file.

```

 FileFormatInfo info = FileFormatUtil.detectFileFormat(getMyDir() + "Document.html");

 Assert.assertEquals(LoadFormat.HTML, info.getLoadFormat());

 // The Encoding property is used only when we create a FileFormatInfo object for an html document.
 Assert.assertEquals("windows-1252", info.getEncoding().name());
 
```

**Returns:**
java.nio.charset.Charset - The detected encoding if applicable to the current document format.
### getLoadFormat() {#getLoadFormat}
```
public int getLoadFormat()
```


Gets the detected document format.

 **Remarks:** 

When an OOXML document is encrypted, it is not possible to ascertained whether it is an Excel, Word or PowerPoint document without decrypting it first so for an encrypted OOXML document this property will always return [LoadFormat.DOCX](../../com.aspose.words/loadformat/\#DOCX).

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

Shows how to use the FileFormatUtil methods to detect the format of a document.

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
int - The detected document format. The returned value is one of [LoadFormat](../../com.aspose.words/loadformat/) constants.
### hasDigitalSignature() {#hasDigitalSignature}
```
public boolean hasDigitalSignature()
```


Returns  true  if this document contains a digital signature. This property merely informs that a digital signature is present on a document, but it does not specify whether the signature is valid or not.

 **Remarks:** 

This property exists to help you sort documents that are digitally signed from those that are not. If you use Aspose.Words to modify and save a document that is digitally signed, then the digital signature will be lost. This is by design because a digital signature exists to guard the authenticity of a document. Using this property you can detect digitally signed documents before processing them in the same way as normal documents and take some action to avoid losing the digital signature, for example notify the user.

 **Examples:** 

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

**Returns:**
boolean -  true  if this document contains a digital signature.
### hasMacros() {#hasMacros}
```
public boolean hasMacros()
```


Returns  true  if this document contains a VBA macros.

 **Examples:** 

Shows how to check VBA macro presence without loading document.

```

 FileFormatInfo fileFormatInfo = FileFormatUtil.detectFileFormat(getMyDir() + "Macro.docm");
 Assert.assertTrue(fileFormatInfo.hasMacros());
 
```

**Returns:**
boolean -  true  if this document contains a VBA macros.
### isEncrypted() {#isEncrypted}
```
public boolean isEncrypted()
```


Returns  true  if the document is encrypted and requires a password to open.

 **Remarks:** 

This property exists to help you sort documents that are encrypted from those that are not. If you attempt to load an encrypted document using Aspose.Words without supplying a password an exception will be thrown. You can use this property to detect whether a document requires a password and take some action before loading a document, for example, prompt the user for a password.

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

**Returns:**
boolean -  true  if the document is encrypted and requires a password to open.
