---
title: Class DigitalSignatureUtil
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.DigitalSignatures.DigitalSignatureUtil klas. Stellt Methoden zum Signieren von Dokumenten bereit.
type: docs
weight: 410
url: /de/net/aspose.words.digitalsignatures/digitalsignatureutil/
---
## DigitalSignatureUtil class

Stellt Methoden zum Signieren von Dokumenten bereit.

Um mehr zu erfahren, besuchen Sie die[Arbeiten Sie mit digitalen Signaturen](https://docs.aspose.com/words/net/working-with-digital-signatures/) Dokumentationsartikel.

```csharp
public static class DigitalSignatureUtil
```

## Methoden

| Name | Beschreibung |
| --- | --- |
| static [LoadSignatures](../../aspose.words.digitalsignatures/digitalsignatureutil/loadsignatures/#loadsignatures)(Stream) | Lädt digitale Signaturen aus dem Dokument mit stream. |
| static [LoadSignatures](../../aspose.words.digitalsignatures/digitalsignatureutil/loadsignatures/#loadsignatures_1)(string) | Lädt digitale Signaturen aus dem Dokument. |
| static [RemoveAllSignatures](../../aspose.words.digitalsignatures/digitalsignatureutil/removeallsignatures/#removeallsignatures)(Stream, Stream) | Entfernt alle digitalen Signaturen vom Dokument im Quellstream und schreibt das nicht signierte Dokument in den Zielstream. |
| static [RemoveAllSignatures](../../aspose.words.digitalsignatures/digitalsignatureutil/removeallsignatures/#removeallsignatures_1)(string, string) | Entfernt alle digitalen Signaturen aus der Quelldatei und schreibt die nicht signierte Datei in die Zieldatei. |
| static [Sign](../../aspose.words.digitalsignatures/digitalsignatureutil/sign/#sign)(Stream, Stream, CertificateHolder) | Signiert das Quelldokument mit der angegebenen[`CertificateHolder`](../certificateholder/)mit digitaler Signatur und schreibt signiertes Dokument in den Zielstream. |
| static [Sign](../../aspose.words.digitalsignatures/digitalsignatureutil/sign/#sign_2)(string, string, CertificateHolder) | Signiert das Quelldokument mit der angegebenen[`CertificateHolder`](../certificateholder/) mit digitaler Signatur und schreibt signiertes Dokument in die Zieldatei. |
| static [Sign](../../aspose.words.digitalsignatures/digitalsignatureutil/sign/#sign_1)(Stream, Stream, CertificateHolder, SignOptions) | Signiert das Quelldokument mit der angegebenen[`CertificateHolder`](../certificateholder/) Und[`SignOptions`](../signoptions/) mit digitaler Signatur und schreibt signiertes Dokument in den Zielstream. |
| static [Sign](../../aspose.words.digitalsignatures/digitalsignatureutil/sign/#sign_3)(string, string, CertificateHolder, SignOptions) | Signiert das Quelldokument mit der angegebenen[`CertificateHolder`](../certificateholder/) Und[`SignOptions`](../signoptions/) mit digitaler Signatur und schreibt signiertes Dokument in die Zieldatei. |

### Bemerkungen

Da die digitale Signatur mit Dateiinhalten und nicht mit dem Dokumentobjektmodell arbeitet, werden diese Methoden in eine separate Klasse eingeordnet.

Unterstützte Formate sindDoc UndDocx.

### Beispiele

Zeigt, wie Signaturen aus einem digital signierten Dokument geladen werden.

```csharp
// Es gibt zwei Möglichkeiten, die Sammlung digitaler Signaturen eines signierten Dokuments mithilfe der DigitalSignatureUtil-Klasse zu laden.
// 1 – Aus einem Dokument aus einem lokalen Dateisystem laden Dateiname:
DigitalSignatureCollection digitalSignatures = 
    DigitalSignatureUtil.LoadSignatures(MyDir + "Digitally signed.docx");

// Wenn diese Sammlung nicht leer ist, können wir überprüfen, ob das Dokument digital signiert ist.
Assert.AreEqual(1, digitalSignatures.Count);

// 2 – Aus einem Dokument aus einem FileStream laden:
using (Stream stream = new FileStream(MyDir + "Digitally signed.docx", FileMode.Open))
{
    digitalSignatures = DigitalSignatureUtil.LoadSignatures(stream);
    Assert.AreEqual(1, digitalSignatures.Count);
}
```

Zeigt, wie digitale Signaturen aus einem digital signierten Dokument entfernt werden.

```csharp
// Es gibt zwei Möglichkeiten, die DigitalSignatureUtil-Klasse zum Entfernen digitaler Signaturen zu verwenden
// aus einem signierten Dokument, indem Sie eine unsignierte Kopie davon irgendwo anders im lokalen Dateisystem speichern.
// 1 – Bestimmen Sie die Speicherorte sowohl des signierten Dokuments als auch der nicht signierten Kopie anhand von Dateinamenszeichenfolgen:
DigitalSignatureUtil.RemoveAllSignatures(MyDir + "Digitally signed.docx",
    ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromString.docx");

// 2 – Bestimmen Sie die Speicherorte sowohl des signierten Dokuments als auch der nicht signierten Kopie anhand von Dateiströmen:
using (Stream streamIn = new FileStream(MyDir + "Digitally signed.docx", FileMode.Open))
{
    using (Stream streamOut = new FileStream(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromStream.docx", FileMode.Create))
    {
        DigitalSignatureUtil.RemoveAllSignatures(streamIn, streamOut);
    }
}

// Stellen Sie sicher, dass unsere beiden Ausgabedokumente keine digitalen Signaturen haben.
Assert.That(DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromString.docx"), Is.Empty);
Assert.That(DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromStream.docx"), Is.Empty);
```

### Siehe auch

* namensraum [Aspose.Words.DigitalSignatures](../../aspose.words.digitalsignatures/)
* Montage [Aspose.Words](../../)


