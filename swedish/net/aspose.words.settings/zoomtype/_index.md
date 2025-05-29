---
title: ZoomType Enum
linktitle: ZoomType
articleTitle: ZoomType
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.Settings.ZoomType-enum för att anpassa dokumentvisningsstorlekar i Microsoft Word för optimal visning och produktivitet.
type: docs
weight: 6810
url: /sv/net/aspose.words.settings/zoomtype/
---
## ZoomType enumeration

Möjliga värden för hur stort eller litet dokumentet visas på skärmen i Microsoft Word.

```csharp
public enum ZoomType
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Custom | `0` | Zoomprocenten är explicit inställd. Den beräknas inte om automatiskt när kontrollstorleken ändras. |
| None | `0` | Indikerar att den explicita zoomprocenten ska användas. Samma somCustom . |
| FullPage | `1` | Zoomprocenten beräknas automatiskt om för att passa en hel sida. |
| PageWidth | `2` | Zoomprocenten beräknas automatiskt om för att passa sidbredden. |
| TextFit | `3` | Zoomprocenten beräknas automatiskt om för att passa texten. |

## Exempel

Visar hur man ställer in en anpassad zoomfaktor, som äldre versioner av Microsoft Word kommer att tillämpa på ett dokument vid laddning.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

doc.ViewOptions.ViewType = ViewType.PageLayout;
doc.ViewOptions.ZoomPercent = 50;

Assert.AreEqual(ZoomType.Custom, doc.ViewOptions.ZoomType);
Assert.AreEqual(ZoomType.None, doc.ViewOptions.ZoomType);

doc.Save(ArtifactsDir + "ViewOptions.SetZoomPercentage.doc");
```

### Se även

* class [ViewOptions](../viewoptions/)
* property [ZoomType](../viewoptions/zoomtype/)
* namnutrymme [Aspose.Words.Settings](../../aspose.words.settings/)
* hopsättning [Aspose.Words](../../)
