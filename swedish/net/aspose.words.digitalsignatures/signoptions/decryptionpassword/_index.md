---
title: SignOptions.DecryptionPassword
linktitle: DecryptionPassword
articleTitle: DecryptionPassword
second_title: Aspose.Words för .NET
description: Lås upp dina dokument utan ansträngning med SignOptions DecryptionPassword-funktion. Dekryptera källfiler säkert och enkelt; standardinställningen är en tom sträng.
type: docs
weight: 30
url: /sv/net/aspose.words.digitalsignatures/signoptions/decryptionpassword/
---
## SignOptions.DecryptionPassword property

Lösenordet för att dekryptera källdokumentet. Standardvärdet är**tom sträng** (Empty ).

```csharp
public string DecryptionPassword { get; set; }
```

## Anmärkningar

Om OOXML-dokumentet är krypterat måste du ange dekrypteringslösenordet för att dekryptera källdokumentet innan det signeras. Detta krävs inte för dokument i binärt DOC-format.

## Exempel

Visar hur man signerar en krypterad dokumentfil.

```csharp
// Skapa ett X.509-certifikat från ett PKCS#12-arkiv, vilket ska innehålla en privat nyckel.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// Skapa ett lösenord för kommentar, datum och dekryptering som kommer att tillämpas med vår nya digitala signatur.
SignOptions signOptions = new SignOptions
{
    Comments = "Comment",
    SignTime = DateTime.Now,
    DecryptionPassword = "docPassword"
};

// Ange ett lokalt systemfilnamn för det osignerade indatadokumentet och ett utdatafilnamn för dess nya digitalt signerade kopia.
string inputFileName = MyDir + "Encrypted.docx";
string outputFileName = ArtifactsDir + "DigitalSignatureUtil.DecryptionPassword.docx";

DigitalSignatureUtil.Sign(inputFileName, outputFileName, certificateHolder, signOptions);
```

### Se även

* class [SignOptions](../)
* namnutrymme [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* hopsättning [Aspose.Words](../../../)
