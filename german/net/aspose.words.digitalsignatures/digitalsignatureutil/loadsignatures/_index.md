---
title: DigitalSignatureUtil.LoadSignatures
linktitle: LoadSignatures
articleTitle: LoadSignatures
second_title: Aspose.Words für .NET
description: Laden Sie mühelos digitale Signaturen aus Ihren Dokumenten mit der LoadSignatures-Methode von DigitalSignatureUtil. Optimieren Sie Ihren Workflow noch heute!
type: docs
weight: 10
url: /de/net/aspose.words.digitalsignatures/digitalsignatureutil/loadsignatures/
---
## LoadSignatures(*string*) {#loadsignatures_1}

Lädt digitale Signaturen aus dem Dokument.

```csharp
public static DigitalSignatureCollection LoadSignatures(string fileName)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fileName | String | Pfad zum Dokument. |

### Rückgabewert

Sammlung digitaler Signaturen. Gibt eine leere Sammlung zurück, wenn die Datei nicht signiert ist.

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

* class [DigitalSignatureCollection](../../digitalsignaturecollection/)
* class [DigitalSignatureUtil](../)
* namensraum [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* Montage [Aspose.Words](../../../)

---

## LoadSignatures(*Stream*) {#loadsignatures}

Lädt digitale Signaturen aus dem Dokument mithilfe eines Streams.

```csharp
public static DigitalSignatureCollection LoadSignatures(Stream stream)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| stream | Stream | Streamen Sie mit dem Dokument. |

### Rückgabewert

Sammlung digitaler Signaturen. Gibt eine leere Sammlung zurück, wenn die Datei nicht signiert ist.

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

### Siehe auch

* class [DigitalSignatureCollection](../../digitalsignaturecollection/)
* class [DigitalSignatureUtil](../)
* namensraum [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* Montage [Aspose.Words](../../../)
