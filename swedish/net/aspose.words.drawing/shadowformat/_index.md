---
title: ShadowFormat Class
linktitle: ShadowFormat
articleTitle: ShadowFormat
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.Drawing.ShadowFormat för förbättrade skuggeffekter för objekt. Förhöj din dokumentdesign med anpassningsbara skuggformateringsalternativ.
type: docs
weight: 1620
url: /sv/net/aspose.words.drawing/shadowformat/
---
## ShadowFormat class

Representerar skuggformatering för ett objekt.

För att lära dig mer, besök[Arbeta med grafiska element](https://docs.aspose.com/words/net/working-with-graphic-elements/) dokumentationsartikel.

```csharp
public class ShadowFormat
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Color](../../aspose.words.drawing/shadowformat/color/) { get; } | Får enColor objektet som representerar färgen för skuggan. Standardvärdet ärBlack . |
| [Type](../../aspose.words.drawing/shadowformat/type/) { get; set; } | Hämtar eller ställer in det angivna[`ShadowType`](../shadowtype/) för ShadowFormat. |
| [Visible](../../aspose.words.drawing/shadowformat/visible/) { get; } | Returer`sann` om formateringen som tillämpats på den här instansen är synlig. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [Clear](../../aspose.words.drawing/shadowformat/clear/)() | Rensar skuggformat. |

## Exempel

Visar hur man får skuggfärg.

```csharp
Document doc = new Document(MyDir + "Shadow color.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
ShadowFormat shadowFormat = shape.ShadowFormat;

Assert.AreEqual(Color.Red.ToArgb(), shadowFormat.Color.ToArgb());
Assert.AreEqual(ShadowType.ShadowMixed, shadowFormat.Type);
```

### Se även

* namnutrymme [Aspose.Words.Drawing](../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../)
