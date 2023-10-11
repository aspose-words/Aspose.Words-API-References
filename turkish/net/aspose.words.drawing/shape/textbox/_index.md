---
title: Shape.TextBox
second_title: Aspose.Words for .NET API Referansı
description: Shape mülk. Metnin bir şekilde nasıl görüntüleneceğini belirten nitelikleri tanımlar.
type: docs
weight: 220
url: /tr/net/aspose.words.drawing/shape/textbox/
---
## Shape.TextBox property

Metnin bir şekilde nasıl görüntüleneceğini belirten nitelikleri tanımlar.

```csharp
public TextBox TextBox { get; }
```

### Örnekler

Bir metin kutusu içindeki metnin yönünün nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 150, 100);
TextBox textBox = textBoxShape.TextBox;

// Belge oluşturucuyu TextBox'un içine taşıyın ve metin ekleyin.
builder.MoveTo(textBoxShape.LastParagraph);
builder.Writeln("Hello world!");
builder.Write("Hello again!");

// Bu metin kutusunun metin içeriğinin yönünü ayarlamak için "LayoutFlow" özelliğini ayarlayın.
textBox.LayoutFlow = layoutFlow;

doc.Save(ArtifactsDir + "Shape.TextBoxLayoutFlow.docx");
```

### Ayrıca bakınız

* class [TextBox](../../textbox/)
* class [Shape](../)
* ad alanı [Aspose.Words.Drawing](../../shape/)
* toplantı [Aspose.Words](../../../)


