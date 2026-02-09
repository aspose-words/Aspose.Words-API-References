---
title: FileFormatInfo Class
linktitle: FileFormatInfo
articleTitle: FileFormatInfo
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.FileFormatInfo class for efficient document format detection. Access detailed data to enhance your file management solutions.
type: docs
weight: 3220
url: /net/aspose.words/fileformatinfo/
---
## FileFormatInfo class

Contains data returned by [`FileFormatUtil`](../fileformatutil/) document format detection methods.

To learn more, visit the [Detect File Format and Check Format Compatibility](https://docs.aspose.com/words/net/detect-file-format-and-check-format-compatibility/) documentation article.

```csharp
public class FileFormatInfo
```

## Properties

| Name | Description |
| --- | --- |
| [Encoding](../../aspose.words/fileformatinfo/encoding/) { get; } | Gets the detected encoding if applicable to the current document format. At the moment detects encoding only for HTML documents. |
| [HasDigitalSignature](../../aspose.words/fileformatinfo/hasdigitalsignature/) { get; } | Returns `true` if this document contains a digital signature. This property merely informs that a digital signature is present on a document, but it does not specify whether the signature is valid or not. |
| [HasMacros](../../aspose.words/fileformatinfo/hasmacros/) { get; } | Returns `true` if this document contains a VBA macros. |
| [IsEncrypted](../../aspose.words/fileformatinfo/isencrypted/) { get; } | Returns `true` if the document is encrypted and requires a password to open. |
| [LoadFormat](../../aspose.words/fileformatinfo/loadformat/) { get; } | Gets the detected document format. |

## Remarks

You do not create instances of this class directly. Objects of this class are returned by [`DetectFileFormat`](../fileformatutil/detectfileformat/) methods.

## Examples

Shows how to use the FileFormatUtil class to detect the document format and encryption.

```csharp
Document doc = new Document();

// Configure a SaveOptions object to encrypt the document
// with a password when we save it, and then save the document.
OdtSaveOptions saveOptions = new OdtSaveOptions(SaveFormat.Odt);
saveOptions.Password = "MyPassword";

doc.Save(ArtifactsDir + "File.DetectDocumentEncryption.odt", saveOptions);

// Verify the file type of our document, and its encryption status.
FileFormatInfo info = FileFormatUtil.DetectFileFormat(ArtifactsDir + "File.DetectDocumentEncryption.odt");

Assert.That(FileFormatUtil.LoadFormatToExtension(info.LoadFormat), Is.EqualTo(".odt"));
Assert.That(info.IsEncrypted, Is.True);
```

Shows how to use the FileFormatUtil class to detect the document format and presence of digital signatures.

```csharp
// Use a FileFormatInfo instance to verify that a document is not digitally signed.
FileFormatInfo info = FileFormatUtil.DetectFileFormat(MyDir + "Document.docx");

Assert.That(FileFormatUtil.LoadFormatToExtension(info.LoadFormat), Is.EqualTo(".docx"));
Assert.That(info.HasDigitalSignature, Is.False);

CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
SignOptions signOptions = new SignOptions() { SignTime = DateTime.Now };
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "File.DetectDigitalSignatures.docx",
    certificateHolder, signOptions);

// Use a new FileFormatInstance to confirm that it is signed.
info = FileFormatUtil.DetectFileFormat(ArtifactsDir + "File.DetectDigitalSignatures.docx");

Assert.That(info.HasDigitalSignature, Is.True);

// We can load and access the signatures of a signed document in a collection like this.
Assert.That(DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "File.DetectDigitalSignatures.docx").Count, Is.EqualTo(1));
```

### See Also

* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
