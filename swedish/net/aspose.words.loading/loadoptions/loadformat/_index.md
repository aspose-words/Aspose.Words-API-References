---
title: LoadOptions.LoadFormat
linktitle: LoadFormat
articleTitle: LoadFormat
second_title: Aspose.Words för .NET
description: Upptäck LoadOptions LoadFormat-egenskapen för att enkelt ange dokumentformat. Optimera inläsningen med standardinställningen Auto för sömlös prestanda.
type: docs
weight: 90
url: /sv/net/aspose.words.loading/loadoptions/loadformat/
---
## LoadOptions.LoadFormat property

Anger formatet för det dokument som ska läsas in. Standard ärAuto .

```csharp
public LoadFormat LoadFormat { get; set; }
```

## Anmärkningar

Det rekommenderas att du angerAuto värde och låt Aspose.Words detect filformatet automatiskt. Om du känner till formatet på dokumentet du ska läsa in kan du ange format explicit och detta kommer att minska laddningstiden något med den omkostnad som är förknippad med automatisk detektering av formatet. Om du anger ett explicit laddningsformat och det visar sig vara fel, kommer automatisk detektering att anropas och ett andra försök att läsa in filen kommer att göras.

## Exempel

Visar hur man anger en bas-URI när man öppnar ett HTML-dokument.

```csharp
// Anta att vi vill ladda ett .html-dokument som innehåller en bild länkad av en relativ URI
// medan bilden är på en annan plats. I så fall måste vi omvandla den relativa URI:n till en absolut.
 // Vi kan tillhandahålla en bas-URI med hjälp av ett HtmlLoadOptions-objekt.
HtmlLoadOptions loadOptions = new HtmlLoadOptions(LoadFormat.Html, "", ImageDir);

Assert.AreEqual(LoadFormat.Html, loadOptions.LoadFormat);

Document doc = new Document(MyDir + "Missing image.html", loadOptions);

// Även om bilden i indata-.html-filen var trasig, hjälpte vår anpassade bas-URI oss att reparera länken.
Shape imageShape = (Shape)doc.GetChildNodes(NodeType.Shape, true)[0];
Assert.True(imageShape.IsImage);

// Detta utdatadokument visar bilden som saknades.
doc.Save(ArtifactsDir + "HtmlLoadOptions.BaseUri.docx");
```

### Se även

* enum [LoadFormat](../../../aspose.words/loadformat/)
* class [LoadOptions](../)
* namnutrymme [Aspose.Words.Loading](../../../aspose.words.loading/)
* hopsättning [Aspose.Words](../../../)
