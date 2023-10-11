---
title: DigitalSignatureUtil.LoadSignatures
second_title: Aspose.Words für .NET-API-Referenz
description: DigitalSignatureUtil methode. Lädt digitale Signaturen aus dem Dokument.
type: docs
weight: 10
url: /de/net/aspose.words.digitalsignatures/digitalsignatureutil/loadsignatures/
---
## LoadSignatures(string) {#loadsignatures_1}

Lädt digitale Signaturen aus dem Dokument.

```csharp
public static DigitalSignatureCollection LoadSignatures(string fileName)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fileName | String | Pfad zum Dokument. |

### Rückgabewert

Sammlung digitaler Signaturen. Gibt eine leere Sammlung zurück, wenn die Datei nicht signiert ist.

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

* class [DigitalSignatureCollection](../../digitalsignaturecollection/)
* class [DigitalSignatureUtil](../)
* namensraum [Aspose.Words.DigitalSignatures](../../digitalsignatureutil/)
* Montage [Aspose.Words](../../../)

---

## LoadSignatures(Stream) {#loadsignatures}

Lädt digitale Signaturen aus dem Dokument mit stream.

```csharp
public static DigitalSignatureCollection LoadSignatures(Stream stream)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| stream | Stream | Streamen Sie mit dem Dokument. |

### Rückgabewert

Sammlung digitaler Signaturen. Gibt eine leere Sammlung zurück, wenn die Datei nicht signiert ist.

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

### Siehe auch

* class [DigitalSignatureCollection](../../digitalsignaturecollection/)
* class [DigitalSignatureUtil](../)
* namensraum [Aspose.Words.DigitalSignatures](../../digitalsignatureutil/)
* Montage [Aspose.Words](../../../)


