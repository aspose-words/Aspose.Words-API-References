---
title: Shape.FirstParagraph
linktitle: FirstParagraph
articleTitle: FirstParagraph
second_title: .NET için Aspose.Words
description: Bir şeklin ilk paragrafını zahmetsizce alın. Kullanımı kolay Shape FirstParagraph özelliğimizle belgenizin düzenini geliştirin.
type: docs
weight: 70
url: /tr/net/aspose.words.drawing/shape/firstparagraph/
---
## Shape.FirstParagraph property

Şekildeki ilk paragrafı alır.

```csharp
public Paragraph FirstParagraph { get; }
```

## Örnekler

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

* class [Paragraph](../../../aspose.words/paragraph/)
* class [Shape](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
