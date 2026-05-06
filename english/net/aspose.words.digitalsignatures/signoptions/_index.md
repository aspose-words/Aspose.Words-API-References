---
title: SignOptions Class
linktitle: SignOptions
articleTitle: SignOptions
second_title: Aspose.Words for .NET
description: Discover Aspose.Words.DigitalSignatures.SignOptions class to customize your document signing process with flexible and secure options for enhanced workflow.
type: docs
weight: 620
url: /net/aspose.words.digitalsignatures/signoptions/
---
## SignOptions class

Allows to specify options for document signing.

To learn more, visit the [Work with Digital Signatures](https://docs.aspose.com/words/net/working-with-digital-signatures/) documentation article.

```csharp
public class SignOptions
```

## Constructors

| Name | Description |
| --- | --- |
| [SignOptions](signoptions/)() | The default constructor. |

## Properties

| Name | Description |
| --- | --- |
| [ApplicationVersion](../../aspose.words.digitalsignatures/signoptions/applicationversion/) { get; set; } | Gets or sets the application version for the digital signature. Default value is "12.0". |
| [ColorDepth](../../aspose.words.digitalsignatures/signoptions/colordepth/) { get; set; } | Gets or sets the color depth for the digital signature. Default value is 32. |
| [Comments](../../aspose.words.digitalsignatures/signoptions/comments/) { get; set; } | Specifies comments on the digital signature. Default value is **empty string**(Empty). |
| [DecryptionPassword](../../aspose.words.digitalsignatures/signoptions/decryptionpassword/) { get; set; } | The password to decrypt source document. Default value is **empty string** (Empty). |
| [HorizontalResolution](../../aspose.words.digitalsignatures/signoptions/horizontalresolution/) { get; set; } | Gets or sets the horizontal resolution for the digital signature. Default value is 1920. |
| [OfficeVersion](../../aspose.words.digitalsignatures/signoptions/officeversion/) { get; set; } | Gets or sets the Office version for the digital signature. Default value is "12.0". |
| [ProviderId](../../aspose.words.digitalsignatures/signoptions/providerid/) { get; set; } | Specifies the class ID of the signature provider. Default value is **Empty (all zeroes) Guid**. |
| [SignatureLineId](../../aspose.words.digitalsignatures/signoptions/signaturelineid/) { get; set; } | Signature line identifier. Default value is **Empty (all zeroes) Guid**. |
| [SignatureLineImage](../../aspose.words.digitalsignatures/signoptions/signaturelineimage/) { get; set; } | The image that will be shown in associated [`SignatureLine`](../../aspose.words.drawing/signatureline/). Default value is `null`. |
| [SignTime](../../aspose.words.digitalsignatures/signoptions/signtime/) { get; set; } | The date of signing. Default value is **current time** (Now) |
| [VerticalResolution](../../aspose.words.digitalsignatures/signoptions/verticalresolution/) { get; set; } | Gets or sets the vertical resolution for the digital signature. Default value is 1200. |
| [WindowsVersion](../../aspose.words.digitalsignatures/signoptions/windowsversion/) { get; set; } | Gets or sets the Windows version for the digital signature. Default value is "6.1". |
| [XmlDsigLevel](../../aspose.words.digitalsignatures/signoptions/xmldsiglevel/) { get; set; } | Specifies the level of a digital signature based on XML-DSig standard. The default value is XmlDSig. |

## Examples

Shows how to digitally sign documents.

```csharp
// Create an X.509 certificate from a PKCS#12 store, which should contain a private key.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// Create a comment and date which will be applied with our new digital signature.
SignOptions signOptions = new SignOptions
{
    Comments = "My comment", 
    SignTime = DateTime.Now
};

// Take an unsigned document from the local file system via a file stream,
// then create a signed copy of it determined by the filename of the output file stream.
using (Stream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (Stream streamOut = new FileStream(ArtifactsDir + "DigitalSignatureUtil.SignDocument.docx", FileMode.OpenOrCreate))
    {
        DigitalSignatureUtil.Sign(streamIn, streamOut, certificateHolder, signOptions);
    }
}
```

### See Also

* namespace [Aspose.Words.DigitalSignatures](../../aspose.words.digitalsignatures/)
* assembly [Aspose.Words](../../)
