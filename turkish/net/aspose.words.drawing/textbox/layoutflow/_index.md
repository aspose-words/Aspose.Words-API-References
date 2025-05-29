---
title: TextBox.LayoutFlow
linktitle: LayoutFlow
articleTitle: LayoutFlow
second_title: .NET için Aspose.Words
description: TextBox LayoutFlow özelliğinin şekillerdeki metin düzenini nasıl geliştirdiğini, projeleriniz için tasarım esnekliğini ve okunabilirliği nasıl artırdığını keşfedin.
type: docs
weight: 60
url: /tr/net/aspose.words.drawing/textbox/layoutflow/
---
## TextBox.LayoutFlow property

Bir şeklin metin düzeninin akışını belirler.

```csharp
public LayoutFlow LayoutFlow { get; set; }
```

## Notlar

Varsayılan değer:Horizontal.

## Örnekler

Bir metin kutusunun içindeki metnin yönünün nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 150, 100);
TextBox textBox = textBoxShape.TextBox;

// Belge oluşturucuyu TextBox'ın içine taşıyın ve metin ekleyin.
builder.MoveTo(textBoxShape.LastParagraph);
builder.Writeln("Hello world!");
builder.Write("Hello again!");

// Bu metin kutusunun metin içeriği için bir yönlendirme belirlemek üzere "LayoutFlow" özelliğini ayarlayın.
textBox.LayoutFlow = layoutFlow;

doc.Save(ArtifactsDir + "Shape.TextBoxLayoutFlow.docx");
```

### Ayrıca bakınız

* enum [LayoutFlow](../../layoutflow/)
* class [TextBox](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
