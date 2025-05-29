---
title: Shape.LastParagraph
linktitle: LastParagraph
articleTitle: LastParagraph
second_title: .NET için Aspose.Words
description: Şeklinizdeki son paragrafı kolayca almak için LastParagraph özelliğine erişin, böylece belgenizin düzenini ve okunabilirliğini artırın.
type: docs
weight: 130
url: /tr/net/aspose.words.drawing/shape/lastparagraph/
---
## Shape.LastParagraph property

Şekildeki son paragrafı alır.

```csharp
public Paragraph LastParagraph { get; }
```

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

* class [Paragraph](../../../aspose.words/paragraph/)
* class [Shape](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
