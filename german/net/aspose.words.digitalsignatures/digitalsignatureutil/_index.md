---
title: DigitalSignatureUtil Class
linktitle: DigitalSignatureUtil
articleTitle: DigitalSignatureUtil
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.DigitalSignatures.DigitalSignatureUtil, um Dokumente einfach mit sicheren digitalen Signaturen zu unterzeichnen. Verbessern Sie noch heute die Dokumentenintegrität!
type: docs
weight: 610
url: /de/net/aspose.words.digitalsignatures/digitalsignatureutil/
---
## DigitalSignatureUtil class

Bietet Methoden zum Signieren von Dokumenten.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit digitalen Signaturen](https://docs.aspose.com/words/net/working-with-digital-signatures/) Dokumentationsartikel.

```csharp
public static class DigitalSignatureUtil
```

## Methoden

| Name | Beschreibung |
| --- | --- |
| static [LoadSignatures](../../aspose.words.digitalsignatures/digitalsignatureutil/loadsignatures/#loadsignatures)(*Stream*) | Lädt digitale Signaturen aus dem Dokument mithilfe eines Streams. |
| static [LoadSignatures](../../aspose.words.digitalsignatures/digitalsignatureutil/loadsignatures/#loadsignatures_1)(*string*) | Lädt digitale Signaturen aus dem Dokument. |
| static [RemoveAllSignatures](../../aspose.words.digitalsignatures/digitalsignatureutil/removeallsignatures/#removeallsignatures)(*Stream, Stream*) | Entfernt alle digitalen Signaturen aus dem Dokument im Quellstream und schreibt das nicht signierte Dokument in den Zielstream. |
| static [RemoveAllSignatures](../../aspose.words.digitalsignatures/digitalsignatureutil/removeallsignatures/#removeallsignatures_1)(*string, string*) | Entfernt alle digitalen Signaturen aus der Quelldatei und schreibt die nicht signierte Datei in die Zieldatei. |
| static [Sign](../../aspose.words.digitalsignatures/digitalsignatureutil/sign/#sign)(*Stream, Stream, [CertificateHolder](../certificateholder/)*) | Signiert das Quelldokument mit der angegebenen[`CertificateHolder`](../certificateholder/) mit digitaler Signatur und schreibt das signierte Dokument in den Zielstream. |
| static [Sign](../../aspose.words.digitalsignatures/digitalsignatureutil/sign/#sign_2)(*string, string, [CertificateHolder](../certificateholder/)*) | Signiert das Quelldokument mit der angegebenen[`CertificateHolder`](../certificateholder/) mit digitaler Signatur und schreibt das signierte Dokument in die Zieldatei. |
| static [Sign](../../aspose.words.digitalsignatures/digitalsignatureutil/sign/#sign_1)(*Stream, Stream, [CertificateHolder](../certificateholder/), [SignOptions](../signoptions/)*) | Signiert das Quelldokument mit der angegebenen[`CertificateHolder`](../certificateholder/) Und[`SignOptions`](../signoptions/) mit digitaler Signatur und schreibt das signierte Dokument in den Zielstream. |
| static [Sign](../../aspose.words.digitalsignatures/digitalsignatureutil/sign/#sign_3)(*string, string, [CertificateHolder](../certificateholder/), [SignOptions](../signoptions/)*) | Signiert das Quelldokument mit der angegebenen[`CertificateHolder`](../certificateholder/) Und[`SignOptions`](../signoptions/) mit digitaler Signatur und schreibt das signierte Dokument in die Zieldatei. |

## Bemerkungen

Da die digitale Signatur mit Dateiinhalten und nicht mit dem Document Object Model arbeitet, werden diese Methoden in eine separate Klasse eingefügt.

Unterstützte Formate sind: Doc , Dot , Docx , Dotx , Docm , Dotm , Odt , Ott.

## Beispiele

Zeigt, wie Signaturen aus einem digital signierten Dokument geladen werden.

```csharp
// Es gibt zwei Möglichkeiten, die Sammlung digitaler Signaturen eines signierten Dokuments mithilfe der Klasse DigitalSignatureUtil zu laden.
// 1 - Laden eines Dokuments aus einem lokalen Dateisystem mit Dateinamen:
DigitalSignatureCollection digitalSignatures = 
    DigitalSignatureUtil.LoadSignatures(MyDir + "Digitally signed.docx");

// Wenn diese Sammlung nicht leer ist, können wir überprüfen, ob das Dokument digital signiert ist.
Assert.AreEqual(1, digitalSignatures.Count);

// 2 - Laden eines Dokuments aus einem FileStream:
using (Stream stream = new FileStream(MyDir + "Digitally signed.docx", FileMode.Open))
{
    digitalSignatures = DigitalSignatureUtil.LoadSignatures(stream);
    Assert.AreEqual(1, digitalSignatures.Count);
}
```

Zeigt, wie digitale Signaturen aus einem digital signierten Dokument entfernt werden.

```csharp
// Es gibt zwei Möglichkeiten, die Klasse DigitalSignatureUtil zum Entfernen digitaler Signaturen zu verwenden
// aus einem signierten Dokument, indem Sie eine unsignierte Kopie davon an einer anderen Stelle im lokalen Dateisystem speichern.
// 1 – Bestimmen Sie die Speicherorte des signierten Dokuments und der unsignierten Kopie anhand der Dateinamenzeichenfolgen:
DigitalSignatureUtil.RemoveAllSignatures(MyDir + "Digitally signed.docx",
    ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromString.docx");

// 2 - Bestimmen Sie die Speicherorte des signierten Dokuments und der unsignierten Kopie anhand von Dateiströmen:
using (Stream streamIn = new FileStream(MyDir + "Digitally signed.docx", FileMode.Open))
{
    using (Stream streamOut = new FileStream(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromStream.docx", FileMode.Create))
    {
        DigitalSignatureUtil.RemoveAllSignatures(streamIn, streamOut);
    }
}

// Überprüfen Sie, dass unsere beiden Ausgabedokumente keine digitalen Signaturen haben.
Assert.AreEqual(0, DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromString.docx").Count);
Assert.AreEqual(0, DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromStream.docx").Count);
```

### Siehe auch

* namensraum [Aspose.Words.DigitalSignatures](../../aspose.words.digitalsignatures/)
* Montage [Aspose.Words](../../)
