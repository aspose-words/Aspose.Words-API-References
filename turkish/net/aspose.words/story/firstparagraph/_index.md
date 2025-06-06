---
title: Story.FirstParagraph
linktitle: FirstParagraph
articleTitle: FirstParagraph
second_title: .NET için Aspose.Words
description: Herhangi bir hikayenin ilk paragrafını kolayca çıkarmak, içeriğinizi ve kullanıcı etkileşimini geliştirmek için Story FirstParagraph özelliğini keşfedin.
type: docs
weight: 10
url: /tr/net/aspose.words/story/firstparagraph/
---
## Story.FirstParagraph property

Hikayedeki ilk paragrafı alır.

```csharp
public Paragraph FirstParagraph { get; }
```

## Örnekler

Bir metin dizisinin font özelliğini kullanarak nasıl biçimlendirileceğini gösterir.

```csharp
Document doc = new Document();
Run run = new Run(doc, "Hello world!");

Aspose.Words.Font font = run.Font;
font.Name = "Courier New";
font.Size = 36;
font.HighlightColor = Color.Yellow;

doc.FirstSection.Body.FirstParagraph.AppendChild(run);
doc.Save(ArtifactsDir + "Font.CreateFormattedRun.docx");
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

* class [Paragraph](../../paragraph/)
* class [Story](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
