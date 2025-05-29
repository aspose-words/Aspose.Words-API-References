---
title: ViewOptions.ZoomPercent
linktitle: ZoomPercent
articleTitle: ZoomPercent
second_title: Aspose.Words för .NET
description: Justera egenskapen ZoomPercent i ViewOptions för att ställa in dokumentets zoomnivå mellan 10–500 %. Förbättra läsbarheten och optimera din visningsupplevelse!
type: docs
weight: 50
url: /sv/net/aspose.words.settings/viewoptions/zoompercent/
---
## ViewOptions.ZoomPercent property

Hämtar eller ställer in procentsatsen med vilken du vill visa ditt dokument.

```csharp
public int ZoomPercent { get; set; }
```

## Anmärkningar

Även om Aspose.Words kan läsa och skriva till det här alternativet, är dess användning applikationsspecifik. Till exempel respekterar inte MS Word 2013 värdet av det här alternativet.

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

* class [ViewOptions](../)
* namnutrymme [Aspose.Words.Settings](../../../aspose.words.settings/)
* hopsättning [Aspose.Words](../../../)
