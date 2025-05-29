---
title: TextBox.VerticalAnchor
linktitle: VerticalAnchor
articleTitle: VerticalAnchor
second_title: .NET için Aspose.Words
description: TextBox VerticalAnchor özelliğinin, projelerinizde gelişmiş tasarım ve okunabilirlik için şekiller içindeki metin hizalamasını nasıl geliştirdiğini keşfedin.
type: docs
weight: 120
url: /tr/net/aspose.words.drawing/textbox/verticalanchor/
---
## TextBox.VerticalAnchor property

Bir şekil içindeki metnin dikey hizalamasını belirtir.

```csharp
public TextBoxAnchor VerticalAnchor { get; set; }
```

## Notlar

Varsayılan değer:Top.

## Örnekler

Bir metin kutusunun metin içeriğinin dikey olarak nasıl hizalanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.TextBox, 200, 200);

// "VerticalAnchor" özelliğini "TextBoxAnchor.Top" olarak ayarlayın
// Bu metin kutusundaki metni şeklin üst tarafıyla hizala.
// "VerticalAnchor" özelliğini "TextBoxAnchor.Middle" olarak ayarlayın
// Bu metin kutusundaki metni şeklin ortasına hizala.
// "VerticalAnchor" özelliğini "TextBoxAnchor.Bottom" olarak ayarlayın
// Bu metin kutusundaki metni şeklin altına hizala.
shape.TextBox.VerticalAnchor = verticalAnchor;

builder.MoveTo(shape.FirstParagraph);
builder.Write("Hello world!");

// Metin kutularının içindeki metnin dikey hizalanması Microsoft Word 2007'den itibaren kullanılabilir.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2007);
doc.Save(ArtifactsDir + "Shape.VerticalAnchor.docx");
```

### Ayrıca bakınız

* enum [TextBoxAnchor](../../textboxanchor/)
* class [TextBox](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
