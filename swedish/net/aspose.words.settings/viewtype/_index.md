---
title: ViewType Enum
linktitle: ViewType
articleTitle: ViewType
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.Settings.ViewType-enum för Microsoft Word. Lås upp flexibla visningslägen för att förbättra dokumentpresentationen och användarupplevelsen.
type: docs
weight: 6790
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
| None | `0` | Dokumentet ska visas i programmets standardvy. |
| Reading | `0` | Dokumentet ska visas i programmets standardvy. |
| PageLayout | `1` | Dokumentet ska öppnas i en vy som visar dokumentet som det skrivs ut. |
| Outline | `3` | Dokumentet ska renderas i en vy som är optimerad för att konturera eller skapa långa dokument. |
| Normal | `4` | Dokumentet ska renderas i en vy som är optimerad för att konturera eller skapa långa dokument. |
| Web | `5` | Dokumentet ska renderas i en vy som efterliknar hur dokumentet skulle visas på en webbsida. |

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
* property [ViewType](../viewoptions/viewtype/)
* namnutrymme [Aspose.Words.Settings](../../aspose.words.settings/)
* hopsättning [Aspose.Words](../../)
