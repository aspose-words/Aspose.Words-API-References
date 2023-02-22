---
title: SignOptions.DecryptionPassword
second_title: Aspose.Words för .NET API Referens
description: SignOptions fast egendom. Lösenordet för att dekryptera källdokumentet. Standardvärdet är tom sträng Empty .
type: docs
weight: 30
url: /sv/net/aspose.words.digitalsignatures/signoptions/decryptionpassword/
---
## SignOptions.DecryptionPassword property

Lösenordet för att dekryptera källdokumentet. Standardvärdet är **tom sträng** (Empty ).

```csharp
public string DecryptionPassword { get; set; }
```

### Anmärkningar

Om OOXML-dokument är krypterat, bör du tillhandahålla dekrypteringslösenord för att dekryptera källdokumentet innan det kommer att signeras. Detta krävs inte för dokument i binärt DOC-format.

### Exempel

Visar hur man signerar krypterad dokumentfil.

```csharp
// Skapa ett X.509-certifikat från en PKCS#12-butik, som bör innehålla en privat nyckel.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// Skapa en kommentar, datum och dekrypteringslösenord som kommer att tillämpas med vår nya digitala signatur.
SignOptions signOptions = new SignOptions
{
    Comments = "Comment",
    SignTime = DateTime.Now,
    DecryptionPassword = "docPassword"
};

// Ställ in ett lokalt systemfilnamn för det osignerade indatadokumentet och ett utdatafilnamn för dess nya digitalt signerade kopia.
string inputFileName = MyDir + "Encrypted.docx";
string outputFileName = ArtifactsDir + "DigitalSignatureUtil.DecryptionPassword.docx";

DigitalSignatureUtil.Sign(inputFileName, outputFileName, certificateHolder, signOptions);
```

### Se även

* class [SignOptions](../)
* namnutrymme [Aspose.Words.DigitalSignatures](../../signoptions/)
* hopsättning [Aspose.Words](../../../)


