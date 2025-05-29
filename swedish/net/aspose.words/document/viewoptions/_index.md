---
title: Document.ViewOptions
linktitle: ViewOptions
articleTitle: ViewOptions
second_title: Aspose.Words för .NET
description: Upptäck egenskapen Dokumentvisningsalternativ för att anpassa dina visningsinställningar i Microsoft Word för en skräddarsydd visningsupplevelse.
type: docs
weight: 490
url: /sv/net/aspose.words/document/viewoptions/
---
## Document.ViewOptions property

Ger alternativ för att styra hur dokumentet visas i Microsoft Word.

```csharp
public ViewOptions ViewOptions { get; }
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

* class [ViewOptions](../../../aspose.words.settings/viewoptions/)
* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
