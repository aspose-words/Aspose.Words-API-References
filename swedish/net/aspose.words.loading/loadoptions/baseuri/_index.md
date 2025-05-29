---
title: LoadOptions.BaseUri
linktitle: BaseUri
articleTitle: BaseUri
second_title: Aspose.Words för .NET
description: Upptäck egenskapen LoadOptions BaseUri för att enkelt konvertera relativa URI:er till absoluta ettor i dina dokument. Förbättra din URI-hantering idag!
type: docs
weight: 20
url: /sv/net/aspose.words.loading/loadoptions/baseuri/
---
## LoadOptions.BaseUri property

Hämtar eller ställer in strängen som ska användas för att lösa relativa URI:er som finns i dokumentet till absoluta URI:er vid behov. Kan vara`null` eller tom sträng. Standard är`null` .

```csharp
public string BaseUri { get; set; }
```

## Anmärkningar

Den här egenskapen används för att omvandla relativa URI:er till absoluta värden i följande fall:

1. När man läser in ett HTML-dokument från en ström och dokumentet innehåller bilder med relativa URI:er av typen och inte har någon bas-URI specificerad i BASE HTML-elementet.
2. När man sparar ett dokument till PDF och andra format, för att hämta bilder länkade med relativa URI:er så att bilderna kan sparas i utdatadokumentet.

## Exempel

Visar hur man öppnar ett HTML-dokument med bilder från en ström med hjälp av en bas-URI.

```csharp
using (Stream stream = File.OpenRead(MyDir + "Document.html"))
{
    // Skicka URI:n för basmappen när den laddas
    // så att alla bilder med relativa URI:er i HTML-dokumentet kan hittas.
    LoadOptions loadOptions = new LoadOptions();
    loadOptions.BaseUri = ImageDir;

    Document doc = new Document(stream, loadOptions);

    // Verifiera att dokumentets första form innehåller en giltig bild.
    Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

    Assert.IsTrue(shape.IsImage);
    Assert.IsNotNull(shape.ImageData.ImageBytes);
    Assert.AreEqual(32.0, ConvertUtil.PointToPixel(shape.Width), 0.01);
    Assert.AreEqual(32.0, ConvertUtil.PointToPixel(shape.Height), 0.01);
}
```

### Se även

* class [LoadOptions](../)
* namnutrymme [Aspose.Words.Loading](../../../aspose.words.loading/)
* hopsättning [Aspose.Words](../../../)
