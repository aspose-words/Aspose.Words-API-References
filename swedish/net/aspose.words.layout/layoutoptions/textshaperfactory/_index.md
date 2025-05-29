---
title: LayoutOptions.TextShaperFactory
linktitle: TextShaperFactory
articleTitle: TextShaperFactory
second_title: Aspose.Words för .NET
description: Upptäck LayoutOptions TextShaperFactory-egenskapen för avancerad typografi. Förbättra din rendering med anpassningsbara ITextShaperFactory-implementeringar.
type: docs
weight: 100
url: /sv/net/aspose.words.layout/layoutoptions/textshaperfactory/
---
## LayoutOptions.TextShaperFactory property

Hämtar eller sätter[`ITextShaperFactory`](../../../aspose.words.shaping/itextshaperfactory/) implementering som används för avancerade typografiska renderingsfunktioner.

```csharp
public ITextShaperFactory TextShaperFactory { get; set; }
```

## Exempel

Visar hur man stöder OpenType-funktioner med hjälp av HarfBuzz textformningsmotor.

```csharp
Document doc = new Document(MyDir + "OpenType text shaping.docx");

// Aspose.Words kan använda externt tillhandahållna textformningsobjekt,
// som representerar teckensnitt och beräknar formningsinformation för text.
// En textformningsfabrik är nödvändig för dokument som använder flera teckensnitt.
// När textformaren är fabriksinställd använder layouten OpenType-funktioner.
// En instansegenskap returnerar ett statiskt BasicTextShaperCache-objekt som omsluter HarfBuzzTextShaperFactory.
doc.LayoutOptions.TextShaperFactory = HarfBuzzTextShaperFactory.Instance;

// För närvarande fungerar textformning vid export till PDF- eller XPS-format.
doc.Save(ArtifactsDir + "Document.OpenType.pdf");
```

### Se även

* interface [ITextShaperFactory](../../../aspose.words.shaping/itextshaperfactory/)
* class [LayoutOptions](../)
* namnutrymme [Aspose.Words.Layout](../../../aspose.words.layout/)
* hopsättning [Aspose.Words](../../../)
