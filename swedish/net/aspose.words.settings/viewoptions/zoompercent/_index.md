---
title: ViewOptions.ZoomPercent
linktitle: ZoomPercent
articleTitle: ZoomPercent
second_title: Aspose.Words för .NET
description: ViewOptions ZoomPercent fast egendom. Hämtar eller ställer in procentandelen mellan 10 och 500 som du vill visa ditt dokument med i C#.
type: docs
weight: 50
url: /sv/net/aspose.words.settings/viewoptions/zoompercent/
---
## ViewOptions.ZoomPercent property

Hämtar eller ställer in procentandelen (mellan 10 och 500) som du vill visa ditt dokument med.

```csharp
public int ZoomPercent { get; set; }
```

## Anmärkningar

Om värdet är 0 så använder den här egenskapen 100 istället, annars om värdet är mindre än 10 eller större än 500 kastar denna egenskap.

Även om Aspose.Words kan läsa och skriva detta alternativ, är dess användning applikationsspecifik. Till exempel respekterar MS Word 2013 inte värdet av detta alternativ.

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

### Se även

* class [ViewOptions](../)
* namnutrymme [Aspose.Words.Settings](../../../aspose.words.settings/)
* hopsättning [Aspose.Words](../../../)
