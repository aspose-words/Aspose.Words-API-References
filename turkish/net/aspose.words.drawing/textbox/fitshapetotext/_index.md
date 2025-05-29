---
title: TextBox.FitShapeToText
linktitle: FitShapeToText
articleTitle: FitShapeToText
second_title: .NET için Aspose.Words
description: Microsoft Word'deki FitShapeToText özelliğinin, belge sunumunu geliştirerek şekilleri metninize mükemmel şekilde uyacak şekilde nasıl otomatik olarak ayarladığını keşfedin.
type: docs
weight: 10
url: /tr/net/aspose.words.drawing/textbox/fitshapetotext/
---
## TextBox.FitShapeToText property

Microsoft Word'ün şekli metne uyacak şekilde büyütüp büyütmeyeceğini belirler.

```csharp
public bool FitShapeToText { get; set; }
```

## Notlar

Varsayılan değer:`YANLIŞ`.

## Örnekler

Bir metin kutusunun içeriğini sıkıca sığdırmak için nasıl yeniden boyutlandırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 150, 100);
TextBox textBox = textBoxShape.TextBox;

// Üst şeklin uyması için bu değerleri her iki üyeye de uygulayın
// belirlediğimiz boyutları göz ardı ederek metin içeriğinin etrafına sıkıca oturtuyoruz.
textBox.FitShapeToText = true;
textBox.TextBoxWrapMode = TextBoxWrapMode.None;

builder.MoveTo(textBoxShape.LastParagraph);
builder.Write("Text fit tightly inside textbox.");

doc.Save(ArtifactsDir + "Shape.TextBoxFitShapeToText.docx");
```

### Ayrıca bakınız

* class [TextBox](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
