---
title: ITextShaperFactory.GetTextShaper
linktitle: GetTextShaper
articleTitle: GetTextShaper
second_title: Aspose.Words für .NET
description: Entdecken Sie die GetTextShaper-Methode von ITextShaperFactory, um einen benutzerdefinierten Textformer für Ihre spezifischen Schriftartanforderungen zu erstellen und so Ihr Text-Rendering-Erlebnis zu verbessern.
type: docs
weight: 10
url: /de/net/aspose.words.shaping/itextshaperfactory/gettextshaper/
---
## GetTextShaper(*string, int*) {#gettextshaper_1}

Gibt eine neue Instanz eines Textformers für die Schriftart zurück, die angegeben wurde durch*fontPath* Und*faceIndex* .

```csharp
public ITextShaper GetTextShaper(string fontPath, int faceIndex)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fontPath | String | Ein absoluter Pfad zur Schriftartdatei. |
| faceIndex | Int32 | Ein Index der Schriftart in der TrueType-Schriftartensammlung, oder 0, wenn die angegebene Schriftdatei keine TrueType-Schriftartensammlung ist. |

### Siehe auch

* interface [ITextShaper](../../itextshaper/)
* interface [ITextShaperFactory](../)
* namensraum [Aspose.Words.Shaping](../../../aspose.words.shaping/)
* Montage [Aspose.Words](../../../)

---

## GetTextShaper(*string, byte[], int*) {#gettextshaper}

Gibt eine neue Instanz eines Textformers für die Schriftart zurück, die dargestellt wird durch*fontBlob* Und*faceIndex* .

```csharp
public ITextShaper GetTextShaper(string fontId, byte[] fontBlob, int faceIndex)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fontId | String | Eine eindeutige Kennung, die der bereitgestellten Schriftart eindeutig zugeordnet werden kann*fontBlob* . |
| fontBlob | Byte[] | Byte-Array mit den Schriftdaten. |
| faceIndex | Int32 | Ein Index der Schriftart in der TrueType-Schriftsammlung, oder 0, wenn*fontBlob* ist keine TrueType-Schriftartensammlung. |

### Siehe auch

* interface [ITextShaper](../../itextshaper/)
* interface [ITextShaperFactory](../)
* namensraum [Aspose.Words.Shaping](../../../aspose.words.shaping/)
* Montage [Aspose.Words](../../../)
