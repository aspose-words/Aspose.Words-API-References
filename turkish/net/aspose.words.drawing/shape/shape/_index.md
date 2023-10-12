---
title: Shape.Shape
second_title: Aspose.Words for .NET API Referansı
description: Shape inşaatçı. Yeni bir şekil nesnesi oluşturur.
type: docs
weight: 10
url: /tr/net/aspose.words.drawing/shape/shape/
---
## Shape constructor

Yeni bir şekil nesnesi oluşturur.

```csharp
public Shape(DocumentBase doc, ShapeType shapeType)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| doc | DocumentBase | Sahibi belgesi. |
| shapeType | ShapeType | Oluşturulacak şeklin türü. |

### Notlar

Şekil oluşturduktan sonra istediğiniz şekil özelliklerini belirtmelisiniz.

### Örnekler

Yerel dosya sisteminden bir görüntü içeren şeklin belgeye nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();

// "Shape" sınıfının public yapıcısı "ShapeMarkupLanguage.Vml" işaretleme tipine sahip bir şekil oluşturacaktır.
// SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped gibi ilkel olmayan türde bir şekil oluşturmanız gerekiyorsa,
// TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded veya DiagonalCornersRounded,
// lütfen DocumentBuilder.InsertShape'i kullanın.
Shape shape = new Shape(doc, ShapeType.Image);
shape.ImageData.SetImage(ImageDir + "Windows MetaFile.wmf");
shape.Width = 100;
shape.Height = 100;

doc.FirstSection.Body.FirstParagraph.AppendChild(shape);

doc.Save(ArtifactsDir + "Image.FromFile.docx");
```

Metin kutusunun nasıl oluşturulacağını ve biçimlendirileceğini gösterir.

```csharp
Document doc = new Document();

// Kayan bir metin kutusu oluşturun.
Shape textBox = new Shape(doc, ShapeType.TextBox);
textBox.WrapType = WrapType.None;
textBox.Height = 50;
textBox.Width = 200;

// Şeklin içindeki metnin yatay ve dikey hizalamasını ayarlayın.
textBox.HorizontalAlignment = HorizontalAlignment.Center;
textBox.VerticalAlignment = VerticalAlignment.Top;

// Metin kutusuna bir paragraf ekleyin ve metin kutusunun görüntüleyeceği bir metin dizisi ekleyin.
textBox.AppendChild(new Paragraph(doc));
Paragraph para = textBox.FirstParagraph;
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;
Run run = new Run(doc);
run.Text = "Hello world!";
para.AppendChild(run);

doc.FirstSection.Body.FirstParagraph.AppendChild(textBox);

doc.Save(ArtifactsDir + "Shape.CreateTextBox.docx");
```

### Ayrıca bakınız

* class [DocumentBase](../../../aspose.words/documentbase/)
* enum [ShapeType](../../shapetype/)
* class [Shape](../)
* ad alanı [Aspose.Words.Drawing](../../shape/)
* toplantı [Aspose.Words](../../../)


