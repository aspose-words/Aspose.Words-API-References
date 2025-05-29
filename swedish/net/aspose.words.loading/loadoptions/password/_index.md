---
title: LoadOptions.Password
linktitle: Password
articleTitle: Password
second_title: Aspose.Words för .NET
description: Hantera dina krypterade dokument enkelt med LoadOptions lösenordsfunktion. Ställ in eller hämta ditt lösenord säkert för smidig åtkomst.
type: docs
weight: 110
url: /sv/net/aspose.words.loading/loadoptions/password/
---
## LoadOptions.Password property

Hämtar eller ställer in lösenordet för att öppna ett krypterat dokument. Kan vara`null` eller tom sträng. Standard är`null` .

```csharp
public string Password { get; set; }
```

## Anmärkningar

Du behöver veta lösenordet för att öppna ett krypterat dokument. Om dokumentet inte är krypterat, ställ in det på`null` eller tom sträng.

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

* class [LoadOptions](../)
* namnutrymme [Aspose.Words.Loading](../../../aspose.words.loading/)
* hopsättning [Aspose.Words](../../../)
