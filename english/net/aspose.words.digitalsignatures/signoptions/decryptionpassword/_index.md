---
title: SignOptions.DecryptionPassword
linktitle: DecryptionPassword
articleTitle: DecryptionPassword
second_title: Aspose.Words for .NET
description: Unlock your documents effortlessly with SignOptions' DecryptionPassword feature. Securely decrypt source files with ease; default is an empty string.
type: docs
weight: 30
url: /net/aspose.words.digitalsignatures/signoptions/decryptionpassword/
---
## SignOptions.DecryptionPassword property

The password to decrypt source document. Default value is **empty string** (Empty).

```csharp
public string DecryptionPassword { get; set; }
```

## Remarks

If OOXML document is encrypted, you should provide decryption password to decrypt source document before it will be signed. This is not required for documents in binary DOC format.

## Examples

Shows how to sign encrypted document file.

```csharp
// Create an X.509 certificate from a PKCS#12 store, which should contain a private key.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// Create a comment, date, and decryption password which will be applied with our new digital signature.
SignOptions signOptions = new SignOptions
{
    Comments = "Comment",
    SignTime = DateTime.Now,
    DecryptionPassword = "docPassword"
};

// Set a local system filename for the unsigned input document, and an output filename for its new digitally signed copy.
string inputFileName = MyDir + "Encrypted.docx";
string outputFileName = ArtifactsDir + "DigitalSignatureUtil.DecryptionPassword.docx";

DigitalSignatureUtil.Sign(inputFileName, outputFileName, certificateHolder, signOptions);
```

### See Also

* class [SignOptions](../)
* namespace [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* assembly [Aspose.Words](../../../)
