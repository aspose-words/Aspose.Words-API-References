---
title: SignOptions.SignTime
linktitle: SignTime
articleTitle: SignTime
second_title: Aspose.Words för .NET
description: Upptäck SignOptions SignTime för enkel signering. Ställ enkelt in signeringsdatumet med standardinställningen aktuell tid. Effektivisera din dokumentprocess!
type: docs
weight: 70
url: /sv/net/aspose.words.digitalsignatures/signoptions/signtime/
---
## SignOptions.SignTime property

Datum för underskrift. Standardvärdet är**aktuell tid** (Now)

```csharp
public DateTime SignTime { get; set; }
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
