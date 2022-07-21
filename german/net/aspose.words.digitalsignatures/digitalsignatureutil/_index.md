---
title: DigitalSignatureUtil
second_title: Aspose.Words für .NET-API-Referenz
description: Stellt Methoden zum Signieren von Dokumenten bereit.
type: docs
weight: 400
url: /de/net/aspose.words.digitalsignatures/digitalsignatureutil/
---
## DigitalSignatureUtil class

Stellt Methoden zum Signieren von Dokumenten bereit.

```csharp
public static class DigitalSignatureUtil
```

## Methoden

| Name | Beschreibung |
| --- | --- |
| static [LoadSignatures](../../aspose.words.digitalsignatures/digitalsignatureutil/loadsignatures#loadsignatures)(Stream) | Lädt digitale Signaturen aus dem Dokument mit Stream. |
| static [LoadSignatures](../../aspose.words.digitalsignatures/digitalsignatureutil/loadsignatures#loadsignatures_1)(string) | Lädt digitale Signaturen aus dem Dokument. |
| static [RemoveAllSignatures](../../aspose.words.digitalsignatures/digitalsignatureutil/removeallsignatures#removeallsignatures)(Stream, Stream) | Entfernt alle digitalen Signaturen aus dem Dokument im Quellstream und schreibt das unsignierte Dokument in den Zielstream. |
| static [RemoveAllSignatures](../../aspose.words.digitalsignatures/digitalsignatureutil/removeallsignatures#removeallsignatures_1)(string, string) | Entfernt alle digitalen Signaturen aus der Quelldatei und schreibt die unsignierte Datei in die Zieldatei. |
| static [Sign](../../aspose.words.digitalsignatures/digitalsignatureutil/sign#sign)(Stream, Stream, CertificateHolder) | Signiert Quelldokument mit gegeben[`CertificateHolder`](../certificateholder)mit digitaler Signatur und schreibt signiertes Dokument in Zielstream. |
| static [Sign](../../aspose.words.digitalsignatures/digitalsignatureutil/sign#sign_2)(string, string, CertificateHolder) | Signiert Quelldokument mit gegeben[`CertificateHolder`](../certificateholder) mit digitaler Signatur und schreibt signiertes Dokument in Zieldatei. |
| static [Sign](../../aspose.words.digitalsignatures/digitalsignatureutil/sign#sign_1)(Stream, Stream, CertificateHolder, SignOptions) | Signiert Quelldokument mit gegeben[`CertificateHolder`](../certificateholder) und[`SignOptions`](../signoptions) mit digitaler Signatur und schreibt signiertes Dokument in Zielstream. |
| static [Sign](../../aspose.words.digitalsignatures/digitalsignatureutil/sign#sign_3)(string, string, CertificateHolder, SignOptions) | Signiert Quelldokument mit gegeben[`CertificateHolder`](../certificateholder) und[`SignOptions`](../signoptions) mit digitaler Signatur und schreibt signiertes Dokument in Zieldatei. |

### Bemerkungen

Da digitale Signaturen eher mit Dateiinhalten als mit Dokumentenobjektmodellen arbeiten, werden diese Methoden in eine separate Klasse gestellt.

Unterstützte Formate sindDoc undDocx.

### Beispiele

Zeigt, wie Signaturen aus einem digital signierten Dokument geladen werden.

```csharp
// Es gibt zwei Möglichkeiten, die Sammlung digitaler Signaturen eines signierten Dokuments mit der DigitalSignatureUtil-Klasse zu laden.
// 1 - Laden von einem Dokument aus einem lokalen Dateisystem Dateiname:
DigitalSignatureCollection digitalSignatures = 
    DigitalSignatureUtil.LoadSignatures(MyDir + "Digitally signed.docx");

// Wenn diese Sammlung nicht leer ist, können wir überprüfen, ob das Dokument digital signiert ist.
Assert.AreEqual(1, digitalSignatures.Count);

// 2 - Laden von einem Dokument aus einem FileStream:
using (Stream stream = new FileStream(MyDir + "Digitally signed.docx", FileMode.Open))
{
    digitalSignatures = DigitalSignatureUtil.LoadSignatures(stream);
    Assert.AreEqual(1, digitalSignatures.Count);
}
```

Zeigt, wie digitale Signaturen aus einem digital signierten Dokument entfernt werden.

```csharp
// Es gibt zwei Möglichkeiten, die DigitalSignatureUtil-Klasse zu verwenden, um digitale Signaturen zu entfernen
// aus einem signierten Dokument, indem Sie eine unsignierte Kopie davon irgendwo anders im lokalen Dateisystem speichern.
// 1 - Ermitteln Sie die Speicherorte sowohl des signierten Dokuments als auch der unsignierten Kopie anhand von Dateinamen-Strings:
DigitalSignatureUtil.RemoveAllSignatures(MyDir + "Digitally signed.docx",
    ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromString.docx");

// 2 - Ermitteln Sie die Speicherorte sowohl des signierten Dokuments als auch der unsignierten Kopie durch Dateistreams:
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

* namensraum [Aspose.Words.DigitalSignatures](../../aspose.words.digitalsignatures)
* Montage [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
