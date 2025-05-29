---
title: DigitalSignatureCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „DigitalSignatureCollection Count“, rufen Sie effizient die Gesamtzahl der Elemente ab und verbessern Sie so Ihr digitales Signaturmanagement.
type: docs
weight: 20
url: /de/net/aspose.words.digitalsignatures/digitalsignaturecollection/count/
---
## DigitalSignatureCollection.Count property

Ruft die Anzahl der in der Sammlung enthaltenen Elemente ab.

```csharp
public int Count { get; }
```

## Beispiele

Zeigt, wie Dokumente mit X.509-Zertifikaten signiert werden.

```csharp
// Überprüfen Sie, ob ein Dokument signiert ist.
Assert.False(FileFormatUtil.DetectFileFormat(MyDir + "Document.docx").HasDigitalSignature);

// Erstellen Sie ein CertificateHolder-Objekt aus einer PKCS12-Datei, das wir zum Signieren des Dokuments verwenden.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);

// Es gibt zwei Möglichkeiten, eine signierte Kopie eines Dokuments im lokalen Dateisystem zu speichern:
// 1 – Kennzeichnen Sie ein Dokument durch einen lokalen Systemdateinamen und speichern Sie eine signierte Kopie an einem durch einen anderen Dateinamen angegebenen Speicherort.
SignOptions signOptions = new SignOptions { SignTime = DateTime.Now };
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "Document.DigitalSignature.docx",
    certificateHolder, signOptions);

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

// 2 – Nehmen Sie ein Dokument aus einem Stream und speichern Sie eine signierte Kopie in einem anderen Stream.
using (FileStream inDoc = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (FileStream outDoc = new FileStream(ArtifactsDir + "Document.DigitalSignature.docx", FileMode.Create))
    {
        DigitalSignatureUtil.Sign(inDoc, outDoc, certificateHolder);
    }
}

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

// Bitte überprüfen Sie, ob alle digitalen Signaturen des Dokuments gültig sind und kontrollieren Sie deren Details.
Document signedDoc = new Document(ArtifactsDir + "Document.DigitalSignature.docx");
DigitalSignatureCollection digitalSignatureCollection = signedDoc.DigitalSignatures;

Assert.True(digitalSignatureCollection.IsValid);
Assert.AreEqual(1, digitalSignatureCollection.Count);
Assert.AreEqual(DigitalSignatureType.XmlDsig, digitalSignatureCollection[0].SignatureType);
Assert.AreEqual("CN=Morzal.Me", signedDoc.DigitalSignatures[0].IssuerName);
Assert.AreEqual("CN=Morzal.Me", signedDoc.DigitalSignatures[0].SubjectName);
```

### Siehe auch

* class [DigitalSignatureCollection](../)
* namensraum [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* Montage [Aspose.Words](../../../)
