---
title: LayoutFlow Enum
linktitle: LayoutFlow
articleTitle: LayoutFlow
second_title: Aspose.Words for .NET
description: Aspose.Words.Drawing.LayoutFlow Sıralama. Bir metin kutusundaki metin düzeninin akışını belirler C#'da.
type: docs
weight: 1100
url: /tr/net/aspose.words.drawing/layoutflow/
---
## LayoutFlow enumeration

Bir metin kutusundaki metin düzeninin akışını belirler.

```csharp
public enum LayoutFlow
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Horizontal | `0` | Metin yatay olarak görüntülenir. |
| TopToBottomIdeographic | `1` | İdeografik metin dikey olarak görüntülenir. |
| BottomToTop | `2` | Metin dikey olarak görüntülenir. |
| TopToBottom | `3` | Metin dikey olarak görüntülenir. |
| HorizontalIdeographic | `4` | İdeografik metin yatay olarak görüntülenir. |
| Vertical | `5` | Metin dikey olarak görüntülenir. |

## Örnekler

Metin kutusuna nasıl metin ekleneceğini ve yönünün nasıl değiştirileceğini gösterir

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textbox = new Shape(doc, ShapeType.TextBox)
{
    Width = 100, 
    Height = 100,
    TextBox = { LayoutFlow = LayoutFlow.BottomToTop }
};

textbox.AppendChild(new Paragraph(doc));
builder.InsertNode(textbox);

builder.MoveTo(textbox.FirstParagraph);
builder.Write("This text is flipped 90 degrees to the left.");

doc.Save(ArtifactsDir + "Drawing.TextBox.docx");
```

### Ayrıca bakınız

* property [LayoutFlow](../textbox/layoutflow/)
* ad alanı [Aspose.Words.Drawing](../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../)
