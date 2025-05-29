---
title: ShapeBase.WrapType
linktitle: WrapType
articleTitle: WrapType
second_title: .NET için Aspose.Words
description: ShapeBase WrapType özelliğini keşfedin, satır içi veya kayan şekilleri kontrol edin ve gelişmiş düzen esnekliği için metin kaydırmayı özelleştirin.
type: docs
weight: 640
url: /tr/net/aspose.words.drawing/shapebase/wraptype/
---
## ShapeBase.WrapType property

Şeklin satır içi mi yoksa yüzen mi olduğunu tanımlar. Yüzen şekiller için şeklin etrafındaki metnin sarma modunu tanımlar.

```csharp
public WrapType WrapType { get; set; }
```

## Notlar

Varsayılan değer:None.

Sadece en üst seviye şekiller için etkilidir.

## Örnekler

Sayfanın ortasına kayan bir resmin nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Üst üste gelen metnin arkasında görünecek yüzen bir resim ekleyin ve onu sayfanın ortasına hizalayın.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;
shape.BehindText = true;
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.HorizontalAlignment = HorizontalAlignment.Center;
shape.VerticalAlignment = VerticalAlignment.Center;

doc.Save(ArtifactsDir + "Image.CreateFloatingPageCenter.docx");
```

Bir metin kutusunun nasıl oluşturulacağını ve biçimlendirileceğini gösterir.

```csharp
Document doc = new Document();

// Yüzen bir metin kutusu oluşturun.
Shape textBox = new Shape(doc, ShapeType.TextBox);
textBox.WrapType = WrapType.None;
textBox.Height = 50;
textBox.Width = 200;

// Şeklin içindeki metnin yatay ve dikey hizalamasını ayarlayın.
textBox.HorizontalAlignment = HorizontalAlignment.Center;
textBox.VerticalAlignment = VerticalAlignment.Top;

// Metin kutusuna bir paragraf ekleyin ve metin kutusunun göstereceği bir metin parçası ekleyin.
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

* enum [WrapType](../../wraptype/)
* class [ShapeBase](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
