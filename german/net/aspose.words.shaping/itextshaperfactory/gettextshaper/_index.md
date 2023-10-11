---
title: ITextShaperFactory.GetTextShaper
second_title: Aspose.Words für .NET-API-Referenz
description: ITextShaperFactory methode. Gibt eine neue Instanz eines Textformers für die von angegebene Schriftart zurückfontPath UndfaceIndex .
type: docs
weight: 10
url: /de/net/aspose.words.shaping/itextshaperfactory/gettextshaper/
---
## GetTextShaper(string, int) {#gettextshaper_1}

Gibt eine neue Instanz eines Textformers für die von angegebene Schriftart zurück*fontPath* Und*faceIndex* .

```csharp
public ITextShaper GetTextShaper(string fontPath, int faceIndex)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fontPath | String | Ein absoluter Pfad zur Schriftartdatei. |
| faceIndex | Int32 | Ein Index der Schriftart in der TrueType-Schriftartsammlung, oder 0, wenn die angegebene Schriftartdatei keine TrueType-Schriftartsammlung ist. |

### Siehe auch

* interface [ITextShaper](../../itextshaper/)
* interface [ITextShaperFactory](../)
* namensraum [Aspose.Words.Shaping](../../itextshaperfactory/)
* Montage [Aspose.Words](../../../)

---

## GetTextShaper(string, byte[], int) {#gettextshaper}

Gibt eine neue Instanz eines Textformers für die durch dargestellte Schriftart zurück*fontBlob* Und*faceIndex* .

```csharp
public ITextShaper GetTextShaper(string fontId, byte[] fontBlob, int faceIndex)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fontId | String | Eine eindeutige Kennung, die der bereitgestellten Schriftart eindeutig zugeordnet werden kann*fontBlob* . |
| fontBlob | Byte[] | Byte-Array mit den Schriftartdaten. |
| faceIndex | Int32 | Ein Index der Schriftart in der TrueType-Schriftartensammlung, oder 0, wenn*fontBlob* ist keine TrueType-Schriftartsammlung. |

### Siehe auch

* interface [ITextShaper](../../itextshaper/)
* interface [ITextShaperFactory](../)
* namensraum [Aspose.Words.Shaping](../../itextshaperfactory/)
* Montage [Aspose.Words](../../../)


