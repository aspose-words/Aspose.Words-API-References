---
title: TextBox.FitShapeToText
second_title: Aspose.Words for .NET API Referansı
description: TextBox mülk. Microsoft Wordün şekli metne sığdırmak için büyütüp büyütmeyeceğini belirler.
type: docs
weight: 10
url: /tr/net/aspose.words.drawing/textbox/fitshapetotext/
---
## TextBox.FitShapeToText property

Microsoft Word'ün şekli metne sığdırmak için büyütüp büyütmeyeceğini belirler.

```csharp
public bool FitShapeToText { get; set; }
```

### Notlar

Varsayılan değer **yanlış**.

### Örnekler

İçeriğini sıkıca sığdırmak için kendisini yeniden boyutlandırmak için bir metin kutusunun nasıl alınacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 150, 100);
TextBox textBox = textBoxShape.TextBox;

// Üst şeklin sığdırılması için bu değerleri her iki üyeye de uygulayın
// belirlediğimiz boyutları göz ardı ederek metin içeriklerinin etrafını sıkıca sarıyoruz.
textBox.FitShapeToText = true;
textBox.TextBoxWrapMode = TextBoxWrapMode.None;

builder.MoveTo(textBoxShape.LastParagraph);
builder.Write("Text fit tightly inside textbox.");

doc.Save(ArtifactsDir + "Shape.TextBoxFitShapeToText.docx");
```

### Ayrıca bakınız

* class [TextBox](../)
* ad alanı [Aspose.Words.Drawing](../../textbox/)
* toplantı [Aspose.Words](../../../)


