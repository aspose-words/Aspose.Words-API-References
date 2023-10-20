---
title: ViewOptions.ViewType
linktitle: ViewType
articleTitle: ViewType
second_title: Aspose.Words för .NET
description: ViewOptions ViewType fast egendom. Styr visningsläget i Microsoft Word i C#.
type: docs
weight: 40
url: /sv/net/aspose.words.settings/viewoptions/viewtype/
---
## ViewOptions.ViewType property

Styr visningsläget i Microsoft Word.

```csharp
public ViewType ViewType { get; set; }
```

## Anmärkningar

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

* enum [ViewType](../../viewtype/)
* class [ViewOptions](../)
* namnutrymme [Aspose.Words.Settings](../../../aspose.words.settings/)
* hopsättning [Aspose.Words](../../../)
