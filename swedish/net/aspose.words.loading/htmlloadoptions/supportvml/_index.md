---
title: HtmlLoadOptions.SupportVml
linktitle: SupportVml
articleTitle: SupportVml
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen HtmlLoadOptions SupportVml förbättrar din webbupplevelse genom att aktivera stöd för VML-bilder för förbättrad grafikkvalitet.
type: docs
weight: 70
url: /sv/net/aspose.words.loading/htmlloadoptions/supportvml/
---
## HtmlLoadOptions.SupportVml property

Hämtar eller ställer in ett värde som anger om VML-avbildningar ska stödjas.

```csharp
public bool SupportVml { get; set; }
```

## Exempel

Visar hur man stöder villkorsstyrda kommentarer när man laddar ett HTML-dokument.

```csharp
HtmlLoadOptions loadOptions = new HtmlLoadOptions();

// Om värdet är sant tar vi hänsyn till VML-kod när vi analyserar det inlästa dokumentet.
loadOptions.SupportVml = supportVml;

// Detta dokument innehåller en JPEG-bild inom taggarna "<!--[if gte vml 1]>",
// och en annan PNG-bild inom taggarna "<![if !vml]>".
// Om vi ställer in flaggan "SupportVml" till "true", så kommer Aspose.Words att ladda JPEG-filen.
// Om vi ställer in denna flagga till "false", kommer Aspose.Words bara att ladda PNG-filen.
Document doc = new Document(MyDir + "VML conditional.htm", loadOptions);

if (supportVml)
    Assert.AreEqual(ImageType.Jpeg, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).ImageData.ImageType);
else
    Assert.AreEqual(ImageType.Png, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).ImageData.ImageType);
```

### Se även

* class [HtmlLoadOptions](../)
* namnutrymme [Aspose.Words.Loading](../../../aspose.words.loading/)
* hopsättning [Aspose.Words](../../../)
