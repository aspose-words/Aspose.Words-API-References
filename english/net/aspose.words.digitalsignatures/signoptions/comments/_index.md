---
title: SignOptions.Comments
linktitle: Comments
articleTitle: Comments
second_title: Aspose.Words for .NET
description: Discover the SignOptions Comments property to enhance your digital signature with custom notes. Improve clarity and communication effortlessly!
type: docs
weight: 20
url: /net/aspose.words.digitalsignatures/signoptions/comments/
---
## SignOptions.Comments property

Specifies comments on the digital signature. Default value is **empty string**(Empty).

```csharp
public string Comments { get; set; }
```

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

* class [SignOptions](../)
* namespace [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* assembly [Aspose.Words](../../../)
