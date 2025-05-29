---
title: SignOptions.Comments
linktitle: Comments
articleTitle: Comments
second_title: Aspose.Words för .NET
description: Upptäck egenskapen SignOptions Comments för att förbättra din digitala signatur med anpassade anteckningar. Förbättra tydlighet och kommunikation utan ansträngning!
type: docs
weight: 20
url: /sv/net/aspose.words.digitalsignatures/signoptions/comments/
---
## SignOptions.Comments property

Anger kommentarer om den digitala signaturen. Standardvärdet är**tom sträng**(Empty ).

```csharp
public string Comments { get; set; }
```

## Exempel

Visar hur man signerar dokument digitalt.

```csharp
// Skapa ett X.509-certifikat från ett PKCS#12-arkiv, vilket ska innehålla en privat nyckel.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// Skapa en kommentar och ett datum som kommer att tillämpas med vår nya digitala signatur.
SignOptions signOptions = new SignOptions
{
    Comments = "My comment", 
    SignTime = DateTime.Now
};

// Hämta ett osignerat dokument från det lokala filsystemet via en filström,
// skapa sedan en signerad kopia av den som bestäms av filnamnet på utdatafilströmmen.
using (Stream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (Stream streamOut = new FileStream(ArtifactsDir + "DigitalSignatureUtil.SignDocument.docx", FileMode.OpenOrCreate))
    {
        DigitalSignatureUtil.Sign(streamIn, streamOut, certificateHolder, signOptions);
    }
}
```

### Se även

* class [SignOptions](../)
* namnutrymme [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* hopsättning [Aspose.Words](../../../)
