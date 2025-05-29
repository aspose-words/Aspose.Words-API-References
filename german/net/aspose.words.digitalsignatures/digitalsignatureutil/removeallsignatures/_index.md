---
title: DigitalSignatureUtil.RemoveAllSignatures
linktitle: RemoveAllSignatures
articleTitle: RemoveAllSignatures
second_title: Aspose.Words für .NET
description: Entfernen Sie mühelos alle digitalen Signaturen mit der RemoveAllSignatures-Methode von DigitalSignatureUtil. Wandeln Sie Ihre signierten Dateien ganz einfach in saubere, unsignierte Versionen um!
type: docs
weight: 20
url: /de/net/aspose.words.digitalsignatures/digitalsignatureutil/removeallsignatures/
---
## RemoveAllSignatures(*string, string*) {#removeallsignatures_1}

Entfernt alle digitalen Signaturen aus der Quelldatei und schreibt die nicht signierte Datei in die Zieldatei.

Die folgenden Formate sind zum Entfernen digitaler Signaturen kompatibel: Doc , Dot , Docx , Dotx , Docm , Dotm , Odt , Ott.

```csharp
public static void RemoveAllSignatures(string srcFileName, string dstFileName)
```

## Beispiele

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

* class [DigitalSignatureUtil](../)
* namensraum [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* Montage [Aspose.Words](../../../)

---

## RemoveAllSignatures(*Stream, Stream*) {#removeallsignatures}

Entfernt alle digitalen Signaturen aus dem Dokument im Quellstream und schreibt das nicht signierte Dokument in den Zielstream.

**Die Ausgabe wird an den Anfang des Streams geschrieben und die Streamgröße wird mit der Inhaltslänge aktualisiert.**

Die folgenden Formate sind zum Entfernen digitaler Signaturen kompatibel: Doc , Dot , Docx , Dotx , Docm , Dotm , Odt , Ott.

```csharp
public static void RemoveAllSignatures(Stream srcStream, Stream dstStream)
```

## Beispiele

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

* class [DigitalSignatureUtil](../)
* namensraum [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* Montage [Aspose.Words](../../../)
