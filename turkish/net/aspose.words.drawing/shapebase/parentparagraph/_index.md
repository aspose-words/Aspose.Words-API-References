---
title: ShapeBase.ParentParagraph
linktitle: ParentParagraph
articleTitle: ParentParagraph
second_title: .NET için Aspose.Words
description: ShapeBase ParentParagraph özelliğini keşfedin; akıcı içerik yönetimi ve gelişmiş organizasyon için hemen üst paragrafa etkili bir şekilde erişin.
type: docs
weight: 430
url: /tr/net/aspose.words.drawing/shapebase/parentparagraph/
---
## ShapeBase.ParentParagraph property

Hemen üst paragrafı döndürür.

```csharp
public Paragraph ParentParagraph { get; }
```

## Notlar

Bir grup şeklinin alt şekilleri ve bir Office Math nesnesinin alt şekilleri için her zaman şunu döndürür:`hükümsüz`.

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

* class [Paragraph](../../../aspose.words/paragraph/)
* class [ShapeBase](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
