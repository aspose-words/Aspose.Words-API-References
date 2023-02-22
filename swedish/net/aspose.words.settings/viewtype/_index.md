---
title: Enum ViewType
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Settings.ViewType uppräkning. Möjliga värden för visningsläget i Microsoft Word.
type: docs
weight: 5660
url: /sv/net/aspose.words.settings/viewtype/
---
## ViewType enumeration

Möjliga värden för visningsläget i Microsoft Word.

```csharp
public enum ViewType
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| None | `0` | Dokumentet ska återges i applikationens standardvy. |
| Reading | `0` | Dokumentet ska återges i applikationens standardvy. |
| PageLayout | `1` | Dokumentet ska öppnas i en vy som visar dokumentet som det kommer att skrivas ut. |
| Outline | `3` | Dokumentet ska återges i en vy som är optimerad för att skissera eller skapa långa dokument. |
| Normal | `4` | Dokumentet ska återges i en vy som är optimerad för att skissera eller skapa långa dokument. |
| Web | `5` | Dokumentet ska återges i en vy som efterliknar hur detta dokument skulle visas på en webbsida. |

### Exempel

Visar hur man ställer in en anpassad zoomfaktor, vilken äldre versioner av Microsoft Word kommer att tillämpa på ett dokument vid inläsning.

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
* property [ViewType](../viewoptions/viewtype/)
* namnutrymme [Aspose.Words.Settings](../../aspose.words.settings/)
* hopsättning [Aspose.Words](../../)


