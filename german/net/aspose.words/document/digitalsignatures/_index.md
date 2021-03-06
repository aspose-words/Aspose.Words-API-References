---
title: DigitalSignatures
second_title: Aspose.Words für .NET-API-Referenz
description: Ruft die Sammlung digitaler Signaturen für dieses Dokument und ihre Validierungsergebnisse ab.
type: docs
weight: 100
url: /de/net/aspose.words/document/digitalsignatures/
---
## Document.DigitalSignatures property

Ruft die Sammlung digitaler Signaturen für dieses Dokument und ihre Validierungsergebnisse ab.

```csharp
public DigitalSignatureCollection DigitalSignatures { get; }
```

### Bemerkungen

Diese Sammlung enthält digitale Signaturen, die aus dem Originaldokument geladen wurden. Diese digitalen Signaturen werden beim Speichern nicht gespeichert[`Document`](../../document) object in eine Datei oder einen Stream, da beim Speichern oder Konvertieren ein Dokument erstellt wird, das sich vom -Original unterscheidet, und die ursprünglichen digitalen Signaturen nicht mehr gültig sind.

Diese Auflistung ist niemals null. Wenn das Dokument nicht signiert ist, enthält es null Elemente.

### Beispiele

Zeigt, wie Informationen zu jeder Signatur in einem Dokument validiert und angezeigt werden.

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

Zeigt, wie Dokumente mit X.509-Zertifikaten signiert werden.

```csharp
// Sicherstellen, dass ein Dokument nicht signiert ist.
Assert.False(FileFormatUtil.DetectFileFormat(MyDir + "Document.docx").HasDigitalSignature);

// Erstellen Sie ein CertificateHolder-Objekt aus einer PKCS12-Datei, mit der wir das Dokument signieren.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);

// Es gibt zwei Möglichkeiten, eine signierte Kopie eines Dokuments im lokalen Dateisystem zu speichern:
// 1 - Kennzeichnen eines Dokuments durch einen lokalen Systemdateinamen und Speichern einer signierten Kopie an einem Ort, der durch einen anderen Dateinamen angegeben ist.
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "Document.DigitalSignature.docx", 
    certificateHolder, new SignOptions() { SignTime = DateTime.Now } );

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

// 2 - Nehmen Sie ein Dokument aus einem Stream und speichern Sie eine signierte Kopie in einem anderen Stream.
using (FileStream inDoc = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (FileStream outDoc = new FileStream(ArtifactsDir + "Document.DigitalSignature.docx", FileMode.Create))
    {
        DigitalSignatureUtil.Sign(inDoc, outDoc, certificateHolder);
    }
}

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

// Bitte überprüfen Sie, ob alle digitalen Signaturen des Dokuments gültig sind, und überprüfen Sie deren Details.
Document signedDoc = new Document(ArtifactsDir + "Document.DigitalSignature.docx");
DigitalSignatureCollection digitalSignatureCollection = signedDoc.DigitalSignatures;

Assert.True(digitalSignatureCollection.IsValid);
Assert.AreEqual(1, digitalSignatureCollection.Count);
Assert.AreEqual(DigitalSignatureType.XmlDsig, digitalSignatureCollection[0].SignatureType);
Assert.AreEqual("CN=Morzal.Me", signedDoc.DigitalSignatures[0].IssuerName);
Assert.AreEqual("CN=Morzal.Me", signedDoc.DigitalSignatures[0].SubjectName);
```

### Siehe auch

* class [DigitalSignatureCollection](../../../aspose.words.digitalsignatures/digitalsignaturecollection)
* class [Document](../../document)
* namensraum [Aspose.Words](../../document)
* Montage [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
