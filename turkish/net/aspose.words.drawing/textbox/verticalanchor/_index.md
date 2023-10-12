---
title: TextBox.VerticalAnchor
second_title: Aspose.Words for .NET API Referansı
description: TextBox mülk. Bir şekil içindeki metnin dikey hizalamasını belirtir.
type: docs
weight: 120
url: /tr/net/aspose.words.drawing/textbox/verticalanchor/
---
## TextBox.VerticalAnchor property

Bir şekil içindeki metnin dikey hizalamasını belirtir.

```csharp
public TextBoxAnchor VerticalAnchor { get; set; }
```

### Notlar

Varsayılan değer:Top.

### Örnekler

Bir metin kutusunun metin içeriğinin dikey olarak nasıl hizalanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.TextBox, 200, 200);

// "VerticalAnchor" özelliğini "TextBoxAnchor.Top" olarak ayarlayın
// bu metin kutusundaki metni şeklin üst tarafıyla hizalayın.
// "VerticalAnchor" özelliğini "TextBoxAnchor.Middle" olarak ayarlayın
// bu metin kutusundaki metni şeklin merkezine hizalayın.
// "VerticalAnchor" özelliğini "TextBoxAnchor.Bottom" olarak ayarlayın
// bu metin kutusundaki metni şeklin alt kısmına hizalayın.
shape.TextBox.VerticalAnchor = verticalAnchor;

builder.MoveTo(shape.FirstParagraph);
builder.Write("Hello world!");

// Metin kutularının içindeki metnin dikey hizalanması Microsoft Word 2007'den itibaren mümkündür.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2007);
doc.Save(ArtifactsDir + "Shape.VerticalAnchor.docx");
```

### Ayrıca bakınız

* enum [TextBoxAnchor](../../textboxanchor/)
* class [TextBox](../)
* ad alanı [Aspose.Words.Drawing](../../textbox/)
* toplantı [Aspose.Words](../../../)


