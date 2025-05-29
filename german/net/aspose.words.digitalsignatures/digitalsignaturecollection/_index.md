---
title: DigitalSignatureCollection Class
linktitle: DigitalSignatureCollection
articleTitle: DigitalSignatureCollection
second_title: Aspose.Words für .NET
description: Entdecken Sie die DigitalSignatureCollection-Klasse von Aspose.Words, die einfachen Zugriff auf eine schreibgeschützte Sammlung digitaler Signaturen für die sichere Dokumentenverwaltung bietet.
type: docs
weight: 590
url: /de/net/aspose.words.digitalsignatures/digitalsignaturecollection/
---
## DigitalSignatureCollection class

Bietet eine schreibgeschützte Sammlung digitaler Signaturen, die an ein Dokument angehängt sind.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit digitalen Signaturen](https://docs.aspose.com/words/net/working-with-digital-signatures/) Dokumentationsartikel.

```csharp
public class DigitalSignatureCollection : IEnumerable<DigitalSignature>
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [DigitalSignatureCollection](digitalsignaturecollection/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Count](../../aspose.words.digitalsignatures/digitalsignaturecollection/count/) { get; } | Ruft die Anzahl der in der Sammlung enthaltenen Elemente ab. |
| [IsValid](../../aspose.words.digitalsignatures/digitalsignaturecollection/isvalid/) { get; } | Rückgaben`WAHR`wenn alle digitalen Signaturen in dieser Sammlung gültig sind und das Dokument nicht manipuliert wurde Gibt außerdem zurück`WAHR` wenn keine digitalen Signaturen vorhanden sind. Gibt zurück`FALSCH` wenn mindestens eine digitale Signatur ungültig ist. |
| [Item](../../aspose.words.digitalsignatures/digitalsignaturecollection/item/) { get; } | Ruft eine Dokumentsignatur am angegebenen Index ab. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [GetEnumerator](../../aspose.words.digitalsignatures/digitalsignaturecollection/getenumerator/)() | Gibt ein Wörterbuch-Enumeratorobjekt zurück, mit dem alle Elemente in der Sammlung durchlaufen werden können. |

## Bemerkungen

[`DigitalSignatures`](../../aspose.words/document/digitalsignatures/)

## Beispiele

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

* class [DigitalSignature](../digitalsignature/)
* namensraum [Aspose.Words.DigitalSignatures](../../aspose.words.digitalsignatures/)
* Montage [Aspose.Words](../../)
