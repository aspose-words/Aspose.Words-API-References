---
title: ShapeBase.ParentParagraph
second_title: Aspose.Words for .NET API Referansı
description: ShapeBase mülk. Doğrudan üst paragrafı döndürür.
type: docs
weight: 410
url: /tr/net/aspose.words.drawing/shapebase/parentparagraph/
---
## ShapeBase.ParentParagraph property

Doğrudan üst paragrafı döndürür.

```csharp
public Paragraph ParentParagraph { get; }
```

### Notlar

Bir grup şeklinin alt şekilleri ve bir Office Math nesnesinin alt şekilleri için her zaman şunu döndürür:`hükümsüz`.

### Örnekler

Metin kutusunun nasıl ekleneceğini ve içeriğinin yazı tipinin nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

Shape shape = builder.InsertShape(ShapeType.TextBox, 300, 50);
builder.MoveTo(shape.LastParagraph);
builder.Write("This text is inside the text box.");

// Metin kutusunu görünürden gizlemek için şeklin "Font" nesnesinin "Gizli" özelliğini "true" olarak ayarlayın
// ve normalde kaplayacağı alanı daraltın.
// Metin kutusunu görünür bırakmak için şeklin "Font" nesnesinin "Gizli" özelliğini "false" olarak ayarlayın.
shape.Font.Hidden = hideShape;

// Şekil görünürse yazı tipi nesnesi aracılığıyla görünümünü değiştireceğiz.
if (!hideShape)
{
    shape.Font.HighlightColor = Color.LightGray;
    shape.Font.Color = Color.Red;
    shape.Font.Underline = Underline.Dash;
}

// Oluşturucuyu metin kutusunun dışına, ana belgeye geri taşıyın.
builder.MoveTo(shape.ParentParagraph);

builder.Writeln("\nThis text is outside the text box.");

doc.Save(ArtifactsDir + "Shape.Font.docx");
```

### Ayrıca bakınız

* class [Paragraph](../../../aspose.words/paragraph/)
* class [ShapeBase](../)
* ad alanı [Aspose.Words.Drawing](../../shapebase/)
* toplantı [Aspose.Words](../../../)


