---
title: ViewOptions.ZoomType
linktitle: ZoomType
articleTitle: ZoomType
second_title: Aspose.Words för .NET
description: Upptäck egenskapen ZoomType i ViewOptions för att enkelt justera zoomnivåer baserat på fönsterstorlek, vilket förbättrar användarupplevelsen och gränssnittsflexibiliteten.
type: docs
weight: 60
url: /sv/net/aspose.words.settings/viewoptions/zoomtype/
---
## ViewOptions.ZoomType property

Hämtar eller ställer in ett zoomvärde baserat på fönstrets storlek.

```csharp
public ZoomType ZoomType { get; set; }
```

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

Visar hur man ställer in en anpassad zoomtyp, som äldre versioner av Microsoft Word kommer att tillämpa på ett dokument vid laddning.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Ställ in egenskapen "ZoomType" till "ZoomType.PageWidth" för att hämta Microsoft Word
// för att automatiskt zooma dokumentet så att det passar sidans bredd.
// Ställ in egenskapen "ZoomType" till "ZoomType.FullPage" för att hämta Microsoft Word
// för att automatiskt zooma dokumentet så att hela första sidan blir synlig.
// Ställ in egenskapen "ZoomType" till "ZoomType.TextFit" för att få Microsoft Word
// för att automatiskt zooma dokumentet så att det passar de inre textmarginalerna på första sidan.
doc.ViewOptions.ZoomType = zoomType;

doc.Save(ArtifactsDir + "ViewOptions.SetZoomType.doc");
```

### Se även

* enum [ZoomType](../../zoomtype/)
* class [ViewOptions](../)
* namnutrymme [Aspose.Words.Settings](../../../aspose.words.settings/)
* hopsättning [Aspose.Words](../../../)
