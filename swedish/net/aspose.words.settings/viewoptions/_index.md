---
title: ViewOptions Class
linktitle: ViewOptions
articleTitle: ViewOptions
second_title: Aspose.Words för .NET
description: Aspose.Words.Settings.ViewOptions klass. Ger olika alternativ som styr hur ett dokument visas i Microsoft Word i C#.
type: docs
weight: 5950
url: /sv/net/aspose.words.settings/viewoptions/
---
## ViewOptions class

Ger olika alternativ som styr hur ett dokument visas i Microsoft Word.

För att lära dig mer, besök[Arbeta med alternativ och utseende av Word-dokument](https://docs.aspose.com/words/net/work-with-word-document-options-and-appearance/) dokumentationsartikel.

```csharp
public class ViewOptions
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [DisplayBackgroundShape](../../aspose.words.settings/viewoptions/displaybackgroundshape/) { get; set; } | Styr visningen av bakgrundsformen i utskriftslayoutvyn. |
| [DoNotDisplayPageBoundaries](../../aspose.words.settings/viewoptions/donotdisplaypageboundaries/) { get; set; } | Stänger av visningen av utrymmet mellan textens överkant och sidans övre kant. |
| [FormsDesign](../../aspose.words.settings/viewoptions/formsdesign/) { get; set; } | Anger om dokumentet är i formulärdesignläge. |
| [ViewType](../../aspose.words.settings/viewoptions/viewtype/) { get; set; } | Styr visningsläget i Microsoft Word. |
| [ZoomPercent](../../aspose.words.settings/viewoptions/zoompercent/) { get; set; } | Hämtar eller ställer in procentandelen (mellan 10 och 500) som du vill visa ditt dokument med. |
| [ZoomType](../../aspose.words.settings/viewoptions/zoomtype/) { get; set; } | Hämtar eller ställer in ett zoomvärde baserat på fönstrets storlek. |

## Exempel

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

Visar hur man ställer in en anpassad zoomtyp, vilka äldre versioner av Microsoft Word som kommer att tillämpas på ett dokument vid inläsning.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Ställ in "ZoomType"-egenskapen till "ZoomType.PageWidth" för att hämta Microsoft Word
// för att automatiskt zooma dokumentet så att det passar sidans bredd.
// Ställ in "ZoomType"-egenskapen till "ZoomType.FullPage" för att hämta Microsoft Word
// för att automatiskt zooma dokumentet för att göra hela första sidan synlig.
// Ställ in "ZoomType"-egenskapen till "ZoomType.TextFit" för att hämta Microsoft Word
// för att automatiskt zooma dokumentet så att det passar de inre textmarginalerna på första sidan.
doc.ViewOptions.ZoomType = zoomType;

doc.Save(ArtifactsDir + "ViewOptions.SetZoomType.doc");
```

### Se även

* class [Document](../../aspose.words/document/)
* property [ViewOptions](../../aspose.words/document/viewoptions/)
* namnutrymme [Aspose.Words.Settings](../../aspose.words.settings/)
* hopsättning [Aspose.Words](../../)
