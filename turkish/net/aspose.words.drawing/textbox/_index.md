---
title: TextBox Class
linktitle: TextBox
articleTitle: TextBox
second_title: .NET için Aspose.Words
description: Belgenizin görsel çekiciliğini ve işlevselliğini artırarak, şekiller içindeki metin gösterimini kolayca özelleştirmek için Aspose.Words.Drawing.TextBox sınıfını keşfedin.
type: docs
weight: 1730
url: /tr/net/aspose.words.drawing/textbox/
---
## TextBox class

Bir metnin bir şekil içinde nasıl görüntüleneceğini belirten nitelikleri tanımlar.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Şekillerle Çalışma](https://docs.aspose.com/words/net/working-with-shapes/) belgeleme makalesi.

```csharp
public class TextBox
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [FitShapeToText](../../aspose.words.drawing/textbox/fitshapetotext/) { get; set; } | Microsoft Word'ün şekli metne uyacak şekilde büyütüp büyütmeyeceğini belirler. |
| [InternalMarginBottom](../../aspose.words.drawing/textbox/internalmarginbottom/) { get; set; } | Bir şekil için iç alt kenar boşluğunu noktalarla belirtir. |
| [InternalMarginLeft](../../aspose.words.drawing/textbox/internalmarginleft/) { get; set; } | Bir şekil için iç sol kenar boşluğunu noktalarla belirtir. |
| [InternalMarginRight](../../aspose.words.drawing/textbox/internalmarginright/) { get; set; } | Bir şekil için iç sağ kenar boşluğunu noktalarla belirtir. |
| [InternalMarginTop](../../aspose.words.drawing/textbox/internalmargintop/) { get; set; } | Bir şekil için iç üst kenar boşluğunu noktalarla belirtir. |
| [LayoutFlow](../../aspose.words.drawing/textbox/layoutflow/) { get; set; } | Bir şeklin metin düzeninin akışını belirler. |
| [Next](../../aspose.words.drawing/textbox/next/) { get; set; } | Bir değeri döndürür veya ayarlar`TextBox` bir sonrakini temsil eden`TextBox`bir dizi şekil halinde. |
| [NoTextRotation](../../aspose.words.drawing/textbox/notextrotation/) { get; set; } | Şekil döndürüldüğünde TextBox'ın metninin dönmemesi gerektiğini belirten bir Boole değeri alır veya ayarlar. |
| [Parent](../../aspose.words.drawing/textbox/parent/) { get; } | için bir üst şekil alır`TextBox` . |
| [Previous](../../aspose.words.drawing/textbox/previous/) { get; } | Bir`TextBox` öncekini temsil eden`TextBox`bir dizi şekil halinde. |
| [TextBoxWrapMode](../../aspose.words.drawing/textbox/textboxwrapmode/) { get; set; } | Metnin bir şeklin içinde nasıl sarılacağını belirler. |
| [VerticalAnchor](../../aspose.words.drawing/textbox/verticalanchor/) { get; set; } | Bir şekil içindeki metnin dikey hizalamasını belirtir. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [BreakForwardLink](../../aspose.words.drawing/textbox/breakforwardlink/)() | Bir sonrakine olan bağlantıyı keser`TextBox` . |
| [IsValidLinkTarget](../../aspose.words.drawing/textbox/isvalidlinktarget/)(*TextBox*) | Bunun olup olmadığını belirler`TextBox` hedefe bağlanabilir`TextBox` . |

## Notlar

Kullanın[`TextBox`](../shape/textbox/) Bir şeklin metin özelliklerine erişmek için özellik. Örnekleri oluşturmazsınız`TextBox` sınıfa doğrudan.

## Örnekler

Bir metin kutusu için iç kenar boşluklarının nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Belirli kenar boşluklarına sahip başka bir metin kutusu ekle.
Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 100, 100);
TextBox textBox = textBoxShape.TextBox;
textBox.InternalMarginTop = 15;
textBox.InternalMarginBottom = 15;
textBox.InternalMarginLeft = 15;
textBox.InternalMarginRight = 15;

builder.MoveTo(textBoxShape.LastParagraph);
builder.Write("Text placed according to textbox margins.");

doc.Save(ArtifactsDir + "Shape.TextBoxMargins.docx");
```

Bir metin kutusunun içindeki metnin yönünün nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 150, 100);
TextBox textBox = textBoxShape.TextBox;

// Belge oluşturucuyu TextBox'ın içine taşıyın ve metin ekleyin.
builder.MoveTo(textBoxShape.LastParagraph);
builder.Writeln("Hello world!");
builder.Write("Hello again!");

// Bu metin kutusunun metin içeriği için bir yönlendirme belirlemek üzere "LayoutFlow" özelliğini ayarlayın.
textBox.LayoutFlow = layoutFlow;

doc.Save(ArtifactsDir + "Shape.TextBoxLayoutFlow.docx");
```

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

* ad alanı [Aspose.Words.Drawing](../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../)
