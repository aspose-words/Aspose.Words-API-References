---
title: ViewOptions Class
linktitle: ViewOptions
articleTitle: ViewOptions
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Settings.ViewOptions för att anpassa dokumentvisningen i Microsoft Word, vilket förbättrar din redigeringsupplevelse och produktivitet.
type: docs
weight: 6780
url: /sv/net/aspose.words.settings/viewoptions/
---
## ViewOptions class

Ger olika alternativ som styr hur ett dokument visas i Microsoft Word.

För att lära dig mer, besök[Arbeta med alternativ och utseende i Word-dokument](https://docs.aspose.com/words/net/work-with-word-document-options-and-appearance/) dokumentationsartikel.

```csharp
public class ViewOptions
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [DisplayBackgroundShape](../../aspose.words.settings/viewoptions/displaybackgroundshape/) { get; set; } | Styr visningen av bakgrundsformen i utskriftslayoutvyn. |
| [DoNotDisplayPageBoundaries](../../aspose.words.settings/viewoptions/donotdisplaypageboundaries/) { get; set; } | Stänger av visningen av avståndet mellan textens överkant och sidans överkant. |
| [FormsDesign](../../aspose.words.settings/viewoptions/formsdesign/) { get; set; } | Anger om dokumentet är i formulärdesignläge. |
| [ViewType](../../aspose.words.settings/viewoptions/viewtype/) { get; set; } | Styr visningsläget i Microsoft Word. |
| [ZoomPercent](../../aspose.words.settings/viewoptions/zoompercent/) { get; set; } | Hämtar eller ställer in procentsatsen med vilken du vill visa ditt dokument. |
| [ZoomType](../../aspose.words.settings/viewoptions/zoomtype/) { get; set; } | Hämtar eller ställer in ett zoomvärde baserat på fönstrets storlek. |

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

* class [Document](../../aspose.words/document/)
* property [ViewOptions](../../aspose.words/document/viewoptions/)
* namnutrymme [Aspose.Words.Settings](../../aspose.words.settings/)
* hopsättning [Aspose.Words](../../)
