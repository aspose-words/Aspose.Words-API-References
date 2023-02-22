---
title: LayoutOptions.TextShaperFactory
second_title: Aspose.Words för .NET API Referens
description: LayoutOptions fast egendom. Hämtar eller sätterITextShaperFactory implementering som används för avancerade typografirenderingsfunktioner.
type: docs
weight: 90
url: /sv/net/aspose.words.layout/layoutoptions/textshaperfactory/
---
## LayoutOptions.TextShaperFactory property

Hämtar eller sätter[`ITextShaperFactory`](../../../aspose.words.shaping/itextshaperfactory/) implementering som används för avancerade typografirenderingsfunktioner.

```csharp
public ITextShaperFactory TextShaperFactory { get; set; }
```

### Exempel

Visar hur man stöder OpenType-funktioner med hjälp av HarfBuzz-motorn för textformning.

```csharp
Document doc = new Document(MyDir + "OpenType text shaping.docx");

// Aspose.Words kan använda externt tillhandahållna textformningsobjekt,
// som representerar teckensnitt och beräkningsformningsinformation för text.
// En textformningsfabrik är nödvändig för dokument som använder flera teckensnitt.
// När textformaren är fabriksinställd använder layouten OpenType-funktioner.
// En Instance-egenskap returnerar ett statiskt BasicTextShaperCache-objekt som omsluter HarfBuzzTextShaperFactory.
doc.LayoutOptions.TextShaperFactory = HarfBuzzTextShaperFactory.Instance;

// För närvarande utförs textformning vid export till PDF- eller XPS-format.
doc.Save(ArtifactsDir + "Document.OpenType.pdf");
```

### Se även

* interface [ITextShaperFactory](../../../aspose.words.shaping/itextshaperfactory/)
* class [LayoutOptions](../)
* namnutrymme [Aspose.Words.Layout](../../layoutoptions/)
* hopsättning [Aspose.Words](../../../)


