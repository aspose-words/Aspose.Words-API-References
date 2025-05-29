---
title: ShapeBase.Font
linktitle: Font
articleTitle: Font
second_title: .NET için Aspose.Words
description: Kolay font biçimlendirme erişimi için ShapeBase Font özelliğini keşfedin. Tasarımlarınızı özelleştirilebilir metin stilleri ve benzersiz tipografi seçenekleriyle geliştirin.
type: docs
weight: 190
url: /tr/net/aspose.words.drawing/shapebase/font/
---
## ShapeBase.Font property

Bu nesnenin yazı tipi biçimlendirmesine erişim sağlar.

```csharp
public Font Font { get; }
```

## Örnekler

Metin kutusu eklemeyi ve içeriğinin yazı tipini ayarlamayı gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

Shape shape = builder.InsertShape(ShapeType.TextBox, 300, 50);
builder.MoveTo(shape.LastParagraph);
builder.Write("This text is inside the text box.");

// Şeklin "Font" nesnesinin "Hidden" özelliğini "true" olarak ayarlayın, böylece metin kutusu görünürden gizlenir
// ve normalde kaplayacağı alanı daraltır.
// Şeklin "Font" nesnesinin "Hidden" özelliğini "false" olarak ayarlayın, böylece metin kutusu görünür kalır.
shape.Font.Hidden = hideShape;

// Şekil görünür durumdaysa, görünümünü font nesnesi aracılığıyla değiştireceğiz.
if (!hideShape)
{
    shape.Font.HighlightColor = Color.LightGray;
    shape.Font.Color = Color.Red;
    shape.Font.Underline = Underline.Dash;
}

// Oluşturucuyu metin kutusundan çıkarıp ana belgeye geri taşı.
builder.MoveTo(shape.ParentParagraph);

builder.Writeln("\nThis text is outside the text box.");

doc.Save(ArtifactsDir + "Shape.Font.docx");
```

### Ayrıca bakınız

* class [Font](../../../aspose.words/font/)
* class [ShapeBase](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
