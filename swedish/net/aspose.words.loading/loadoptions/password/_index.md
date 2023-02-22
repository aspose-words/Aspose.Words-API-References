---
title: LoadOptions.Password
second_title: Aspose.Words för .NET API Referens
description: LoadOptions fast egendom. Hämtar eller ställer in lösenordet för att öppna ett krypterat dokument. Kan vara null eller tom sträng. Standard är null.
type: docs
weight: 110
url: /sv/net/aspose.words.loading/loadoptions/password/
---
## LoadOptions.Password property

Hämtar eller ställer in lösenordet för att öppna ett krypterat dokument. Kan vara null eller tom sträng. Standard är null.

```csharp
public string Password { get; set; }
```

### Anmärkningar

Du måste känna till lösenordet för att öppna ett krypterat dokument. Om dokumentet inte är krypterat, ställ in detta på null eller tom sträng.

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

* class [LoadOptions](../)
* namnutrymme [Aspose.Words.Loading](../../loadoptions/)
* hopsättning [Aspose.Words](../../../)


