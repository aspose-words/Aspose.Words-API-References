---
title: LoadOptions.Password
linktitle: Password
articleTitle: Password
second_title: Aspose.Words for .NET
description: Manage your encrypted documents effortlessly with LoadOptions Password property. Securely set or retrieve your password for seamless access.
type: docs
weight: 110
url: /net/aspose.words.loading/loadoptions/password/
---
## LoadOptions.Password property

Gets or sets the password for opening an encrypted document. Can be `null` or empty string. Default is `null`.

```csharp
public string Password { get; set; }
```

## Remarks

You need to know the password to open an encrypted document. If the document is not encrypted, set this to `null` or empty string.

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

* class [LoadOptions](../)
* namespace [Aspose.Words.Loading](../../../aspose.words.loading/)
* assembly [Aspose.Words](../../../)
