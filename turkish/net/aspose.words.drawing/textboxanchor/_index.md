---
title: TextBoxAnchor Enum
linktitle: TextBoxAnchor
articleTitle: TextBoxAnchor
second_title: .NET için Aspose.Words
description: Şekil metninin hassas dikey hizalaması için Aspose.Words.Drawing.TextBoxAnchor enum'unu keşfedin. Belge biçimlendirmenizi zahmetsizce geliştirin!
type: docs
weight: 1740
url: /tr/net/aspose.words.drawing/textboxanchor/
---
## TextBoxAnchor enumeration

Şekil metni dikey hizalaması için kullanılan değerleri belirtir.

```csharp
public enum TextBoxAnchor
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Top | `0` | Metin, metin kutusunun üstüne hizalanır. |
| Middle | `1` | Metin, metin kutusunun ortasına hizalanır. |
| Bottom | `2` | Metin, metin kutusunun altına hizalanır. |
| TopCentered | `3` | Metin, metin kutusunun üst orta kısmına hizalanır. |
| MiddleCentered | `4` | Metin, metin kutusunun ortasına hizalanır. |
| BottomCentered | `5` | Metin, metin kutusunun alt orta kısmına hizalanır. |
| TopBaseline | `6` | Metin, metin kutusunun üst taban çizgisine hizalanır. |
| BottomBaseline | `7` | Metin, metin kutusunun alt taban çizgisine hizalanır. |
| TopCenteredBaseline | `8` | Metin, metin kutusunun üst orta taban çizgisine hizalanır. |
| BottomCenteredBaseline | `9` | Metin, metin kutusunun alt orta taban çizgisine hizalanır. |

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

* ad alanı [Aspose.Words.Drawing](../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../)
