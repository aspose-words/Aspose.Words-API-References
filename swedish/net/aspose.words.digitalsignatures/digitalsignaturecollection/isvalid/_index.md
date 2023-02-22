---
title: DigitalSignatureCollection.IsValid
second_title: Aspose.Words för .NET API Referens
description: DigitalSignatureCollection fast egendom. ReturnerarSann om alla digitala signaturer i denna samling är giltiga och dokumentet inte har manipulerats returneras ocksåSannom det inte finns några digitala signaturer. Returnerarfalsk om minst en digital signatur är ogiltig.
type: docs
weight: 30
url: /sv/net/aspose.words.digitalsignatures/digitalsignaturecollection/isvalid/
---
## DigitalSignatureCollection.IsValid property

Returnerar`Sann` om alla digitala signaturer i denna samling är giltiga och dokumentet inte har manipulerats returneras också`Sann`om det inte finns några digitala signaturer. Returnerar`falsk` om minst en digital signatur är ogiltig.

```csharp
public bool IsValid { get; }
```

### Exempel

Visar hur man signerar dokument med X.509-certifikat.

```csharp
// Kontrollera att ett dokument inte är signerat.
Assert.False(FileFormatUtil.DetectFileFormat(MyDir + "Document.docx").HasDigitalSignature);

// Skapa ett CertificateHolder-objekt från en PKCS12-fil, som vi kommer att använda för att signera dokumentet.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);

// Det finns två sätt att spara en signerad kopia av ett dokument till det lokala filsystemet:
// 1 - Ange ett dokument med ett lokalt systemfilnamn och spara en signerad kopia på en plats som anges med ett annat filnamn.
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "Document.DigitalSignature.docx", 
    certificateHolder, new SignOptions() { SignTime = DateTime.Now } );

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

// 2 - Ta ett dokument från en stream och spara en signerad kopia till en annan stream.
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

* class [DigitalSignatureCollection](../)
* namnutrymme [Aspose.Words.DigitalSignatures](../../digitalsignaturecollection/)
* hopsättning [Aspose.Words](../../../)


