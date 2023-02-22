---
title: DigitalSignatureUtil.RemoveAllSignatures
second_title: Aspose.Words für .NET-API-Referenz
description: DigitalSignatureUtil methode. Entfernt alle digitalen Signaturen aus der Quelldatei und schreibt die unsignierte Datei in die Zieldatei.
type: docs
weight: 20
url: /de/net/aspose.words.digitalsignatures/digitalsignatureutil/removeallsignatures/
---
## RemoveAllSignatures(string, string) {#removeallsignatures_1}

Entfernt alle digitalen Signaturen aus der Quelldatei und schreibt die unsignierte Datei in die Zieldatei.

```csharp
public static void RemoveAllSignatures(string srcFileName, string dstFileName)
```

### Beispiele

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

* class [DigitalSignatureUtil](../)
* namensraum [Aspose.Words.DigitalSignatures](../../digitalsignatureutil/)
* Montage [Aspose.Words](../../../)

---

## RemoveAllSignatures(Stream, Stream) {#removeallsignatures}

Entfernt alle digitalen Signaturen aus dem Dokument im Quellstream und schreibt das unsignierte Dokument in den Zielstream.

**Die Ausgabe wird an den Anfang des Streams geschrieben und die Streamgröße wird mit der Inhaltslänge aktualisiert.**

```csharp
public static void RemoveAllSignatures(Stream srcStream, Stream dstStream)
```

### Beispiele

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

* class [DigitalSignatureUtil](../)
* namensraum [Aspose.Words.DigitalSignatures](../../digitalsignatureutil/)
* Montage [Aspose.Words](../../../)


