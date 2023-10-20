---
title: LoadOptions.LoadFormat
linktitle: LoadFormat
articleTitle: LoadFormat
second_title: Aspose.Words för .NET
description: LoadOptions LoadFormat fast egendom. Anger formatet på dokumentet som ska laddas. Standard ärAuto  i C#.
type: docs
weight: 90
url: /sv/net/aspose.words.loading/loadoptions/loadformat/
---
## LoadOptions.LoadFormat property

Anger formatet på dokumentet som ska laddas. Standard ärAuto .

```csharp
public LoadFormat LoadFormat { get; set; }
```

## Anmärkningar

Det rekommenderas att du specificerarAuto värde och låt Aspose.Words detektera filformatet automatiskt. Om du känner till formatet på dokumentet som du ska ladda kan du ange format explicit och detta kommer att minska laddningstiden något med den omkostnad som är kopplad till automatisk identifiering av formatet. Om du anger ett explicit laddningsformat kommer det att vända Om det är fel, kommer den automatiska upptäckten att anropas och ett andra försök att ladda filen kommer att göras.

## Exempel

Visar hur du anger en bas-URI när du öppnar ett HTML-dokument.

```csharp
// Anta att vi vill ladda ett .html-dokument som innehåller en bild länkad av en relativ URI
// medan bilden är på en annan plats. I så fall måste vi lösa den relativa URI till en absolut.
 // Vi kan tillhandahålla en bas-URI med hjälp av ett HtmlLoadOptions-objekt.
HtmlLoadOptions loadOptions = new HtmlLoadOptions(LoadFormat.Html, "", ImageDir);

Assert.AreEqual(LoadFormat.Html, loadOptions.LoadFormat);

Document doc = new Document(MyDir + "Missing image.html", loadOptions);

// Medan bilden var trasig i inmatningen .html, hjälpte vår anpassade bas-URI oss att reparera länken.
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
