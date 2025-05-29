---
title: SignOptions Class
linktitle: SignOptions
articleTitle: SignOptions
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.DigitalSignatures.SignOptions för att anpassa din dokumentsigneringsprocess med flexibla och säkra alternativ för förbättrat arbetsflöde.
type: docs
weight: 620
url: /sv/net/aspose.words.digitalsignatures/signoptions/
---
## SignOptions class

Gör det möjligt att ange alternativ för dokumentsignering.

För att lära dig mer, besök[Arbeta med digitala signaturer](https://docs.aspose.com/words/net/working-with-digital-signatures/) dokumentationsartikel.

```csharp
public class SignOptions
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [SignOptions](signoptions/)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Comments](../../aspose.words.digitalsignatures/signoptions/comments/) { get; set; } | Anger kommentarer om den digitala signaturen. Standardvärdet är**tom sträng**(Empty ). |
| [DecryptionPassword](../../aspose.words.digitalsignatures/signoptions/decryptionpassword/) { get; set; } | Lösenordet för att dekryptera källdokumentet. Standardvärdet är**tom sträng** (Empty ). |
| [ProviderId](../../aspose.words.digitalsignatures/signoptions/providerid/) { get; set; } | Anger klass-ID för signaturleverantören. Standardvärdet är**Tom (bara nollor) Guid** . |
| [SignatureLineId](../../aspose.words.digitalsignatures/signoptions/signaturelineid/) { get; set; } | Signaturradsidentifierare. Standardvärdet är**Tom (bara nollor) Guid** . |
| [SignatureLineImage](../../aspose.words.digitalsignatures/signoptions/signaturelineimage/) { get; set; } | Bilden som kommer att visas i associerad[`SignatureLine`](../../aspose.words.drawing/signatureline/) . Standardvärdet är`null` . |
| [SignTime](../../aspose.words.digitalsignatures/signoptions/signtime/) { get; set; } | Datum för underskrift. Standardvärdet är**aktuell tid** (Now) |
| [XmlDsigLevel](../../aspose.words.digitalsignatures/signoptions/xmldsiglevel/) { get; set; } | Anger nivån för en digital signatur baserat på XML-DSig-standarden. Standardvärdet ärXmlDSig . |

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

* namnutrymme [Aspose.Words.DigitalSignatures](../../aspose.words.digitalsignatures/)
* hopsättning [Aspose.Words](../../)
