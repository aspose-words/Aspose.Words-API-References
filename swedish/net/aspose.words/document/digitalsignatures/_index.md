---
title: Document.DigitalSignatures
linktitle: DigitalSignatures
articleTitle: DigitalSignatures
second_title: Aspose.Words för .NET
description: Upptäck egenskapen Digitala signaturer för att enkelt komma åt och validera ett dokuments digitala signaturer. Säkerställ äkthet och säkerhet med lätthet.
type: docs
weight: 110
url: /sv/net/aspose.words/document/digitalsignatures/
---
## Document.DigitalSignatures property

Hämtar samlingen av digitala signaturer för detta dokument och deras valideringsresultat.

```csharp
public DigitalSignatureCollection DigitalSignatures { get; }
```

## Anmärkningar

Den här samlingen innehåller digitala signaturer som laddades från originaldokumentet. Dessa digitala signaturer sparas inte när du sparar detta.[`Document`](../) object till en fil eller ström eftersom att spara eller konvertera kommer att producera ett dokument som skiljer sig från originalet och de ursprungliga digitala signaturerna kommer inte längre att vara giltiga.

Denna samling är aldrig`null`Om dokumentet inte är signerat kommer det att innehålla noll element.

## Exempel

Visar hur man validerar och visar information om varje signatur i ett dokument.

```csharp
Document doc = new Document(MyDir + "Digitally signed.docx");

foreach (DigitalSignature signature in doc.DigitalSignatures)
{
    Console.WriteLine($"{(signature.IsValid ? "Valid" : "Invalid")} signature: ");
    Console.WriteLine($"\tReason:\t{signature.Comments}");
    Console.WriteLine($"\tType:\t{signature.SignatureType}");
    Console.WriteLine($"\tSign time:\t{signature.SignTime}");
    Console.WriteLine($"\tSubject name:\t{signature.CertificateHolder.Certificate.SubjectName}");
    Console.WriteLine($"\tIssuer name:\t{signature.CertificateHolder.Certificate.IssuerName.Name}");
    Console.WriteLine();
}
```

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

* class [DigitalSignatureCollection](../../../aspose.words.digitalsignatures/digitalsignaturecollection/)
* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
