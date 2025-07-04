---
title: FileFormatInfo.HasDigitalSignature
linktitle: HasDigitalSignature
articleTitle: HasDigitalSignature
second_title: Aspose.Words for .NET
description: Discover the FileFormatInfo HasDigitalSignature property—quickly check if your document includes a digital signature, enhancing security and authenticity.
type: docs
weight: 20
url: /net/aspose.words/fileformatinfo/hasdigitalsignature/
---
## FileFormatInfo.HasDigitalSignature property

Returns `true` if this document contains a digital signature. This property merely informs that a digital signature is present on a document, but it does not specify whether the signature is valid or not.

```csharp
public bool HasDigitalSignature { get; }
```

## Remarks

This property exists to help you sort documents that are digitally signed from those that are not. If you use Aspose.Words to modify and save a document that is digitally signed, then the digital signature will be lost. This is by design because a digital signature exists to guard the authenticity of a document. Using this property you can detect digitally signed documents before processing them in the same way as normal documents and take some action to avoid losing the digital signature, for example notify the user.

## Examples

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

* class [FileFormatInfo](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
