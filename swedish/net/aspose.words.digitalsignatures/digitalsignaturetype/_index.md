---
title: DigitalSignatureType Enum
linktitle: DigitalSignatureType
articleTitle: DigitalSignatureType
second_title: Aspose.Words för .NET
description: Upptäck enumerationen Aspose.Words.DigitalSignatures.DigitalSignatureType för att förbättra din dokumentsäkerhet med mångsidiga alternativ för digitala signaturer.
type: docs
weight: 600
url: /sv/net/aspose.words.digitalsignatures/digitalsignaturetype/
---
## DigitalSignatureType enumeration

Anger typen av digital signatur.

```csharp
public enum DigitalSignatureType
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Unknown | `0` | Indikerar ett fel, okänd digital signaturtyp. |
| CryptoApi | `1` | Crypto API-signaturmetoden som används i Microsoft Word 97-2003 .DOC binära dokument. |
| XmlDsig | `2` | XmlDsig-signaturmetoden som används i OOXML- och OpenDocument-dokument. |

## Exempel

Visar hur man signerar dokument med X.509-certifikat.

```csharp
// Verifiera att ett dokument inte är signerat.
Assert.False(FileFormatUtil.DetectFileFormat(MyDir + "Document.docx").HasDigitalSignature);

// Skapa ett CertificateHolder-objekt från en PKCS12-fil, som vi kommer att använda för att signera dokumentet.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);

// Det finns två sätt att spara en signerad kopia av ett dokument i det lokala filsystemet:
// 1 - Ange ett dokument med ett lokalt systemfilnamn och spara en signerad kopia på en plats som anges med ett annat filnamn.
SignOptions signOptions = new SignOptions { SignTime = DateTime.Now };
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "Document.DigitalSignature.docx",
    certificateHolder, signOptions);

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

// 2 - Ta ett dokument från en ström och spara en signerad kopia till en annan ström.
using (FileStream inDoc = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (FileStream outDoc = new FileStream(ArtifactsDir + "Document.DigitalSignature.docx", FileMode.Create))
    {
        DigitalSignatureUtil.Sign(inDoc, outDoc, certificateHolder);
    }
}

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

// Kontrollera att alla dokumentets digitala signaturer är giltiga och kontrollera deras uppgifter.
Document signedDoc = new Document(ArtifactsDir + "Document.DigitalSignature.docx");
DigitalSignatureCollection digitalSignatureCollection = signedDoc.DigitalSignatures;

Assert.True(digitalSignatureCollection.IsValid);
Assert.AreEqual(1, digitalSignatureCollection.Count);
Assert.AreEqual(DigitalSignatureType.XmlDsig, digitalSignatureCollection[0].SignatureType);
Assert.AreEqual("CN=Morzal.Me", signedDoc.DigitalSignatures[0].IssuerName);
Assert.AreEqual("CN=Morzal.Me", signedDoc.DigitalSignatures[0].SubjectName);
```

### Se även

* namnutrymme [Aspose.Words.DigitalSignatures](../../aspose.words.digitalsignatures/)
* hopsättning [Aspose.Words](../../)
