---
title: TextBox.LayoutFlow
second_title: Aspose.Words for .NET API Referansı
description: TextBox mülk. Şekildeki metin düzeninin akışını belirler.
type: docs
weight: 60
url: /tr/net/aspose.words.drawing/textbox/layoutflow/
---
## TextBox.LayoutFlow property

Şekildeki metin düzeninin akışını belirler.

```csharp
public LayoutFlow LayoutFlow { get; set; }
```

### Notlar

Varsayılan değer:Horizontal.

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

* enum [LayoutFlow](../../layoutflow/)
* class [TextBox](../)
* ad alanı [Aspose.Words.Drawing](../../textbox/)
* toplantı [Aspose.Words](../../../)


