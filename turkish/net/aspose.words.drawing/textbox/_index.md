---
title: Class TextBox
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Drawing.TextBox sınıf. Metnin şeklin içinde nasıl görüntüleneceğini belirten nitelikleri tanımlar.
type: docs
weight: 1320
url: /tr/net/aspose.words.drawing/textbox/
---
## TextBox class

Metnin şeklin içinde nasıl görüntüleneceğini belirten nitelikleri tanımlar.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Şekillerle Çalışmak](https://docs.aspose.com/words/net/working-with-shapes/) dokümantasyon makalesi.

```csharp
public class TextBox
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [FitShapeToText](../../aspose.words.drawing/textbox/fitshapetotext/) { get; set; } | Microsoft Word'ün şekli metne sığacak şekilde büyütüp büyütmeyeceğini belirler. |
| [InternalMarginBottom](../../aspose.words.drawing/textbox/internalmarginbottom/) { get; set; } | Şeklin iç alt kenar boşluğunu nokta cinsinden belirtir. |
| [InternalMarginLeft](../../aspose.words.drawing/textbox/internalmarginleft/) { get; set; } | Şeklin iç sol kenar boşluğunu nokta cinsinden belirtir. |
| [InternalMarginRight](../../aspose.words.drawing/textbox/internalmarginright/) { get; set; } | Bir şeklin sağ iç kenar boşluğunu nokta cinsinden belirtir. |
| [InternalMarginTop](../../aspose.words.drawing/textbox/internalmargintop/) { get; set; } | Şeklin iç üst kenar boşluğunu nokta cinsinden belirtir. |
| [LayoutFlow](../../aspose.words.drawing/textbox/layoutflow/) { get; set; } | Şekildeki metin düzeninin akışını belirler. |
| [Next](../../aspose.words.drawing/textbox/next/) { get; set; } | Bir değeri döndürür veya ayarlar`TextBox` bu bir sonrakini temsil ediyor`TextBox` bir dizi şekil halinde. |
| [NoTextRotation](../../aspose.words.drawing/textbox/notextrotation/) { get; set; } | Şekil döndürüldüğünde TextBox metninin de dönmemesi gerektiğini belirten bir boole değeri alır veya ayarlar. |
| [Parent](../../aspose.words.drawing/textbox/parent/) { get; } | Bir ana şekil alır`TextBox` . |
| [Previous](../../aspose.words.drawing/textbox/previous/) { get; } | Bir değeri döndürür`TextBox` öncekini temsil eden`TextBox` bir dizi şekil halinde. |
| [TextBoxWrapMode](../../aspose.words.drawing/textbox/textboxwrapmode/) { get; set; } | Metnin şeklin içinde nasıl kaydırılacağını belirler. |
| [VerticalAnchor](../../aspose.words.drawing/textbox/verticalanchor/) { get; set; } | Bir şekil içindeki metnin dikey hizalamasını belirtir. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [BreakForwardLink](../../aspose.words.drawing/textbox/breakforwardlink/)() | Sonrakine olan bağlantıyı keser`TextBox` . |
| [IsValidLinkTarget](../../aspose.words.drawing/textbox/isvalidlinktarget/)(TextBox) | Bunun olup olmadığını belirler`TextBox` hedefe bağlanabilir`TextBox` . |

### Notlar

Kullan[`TextBox`](../shape/textbox/) bir şeklin metin özelliklerine erişim özelliği. Şeklin örneklerini oluşturmazsınız`TextBox` doğrudan sınıf.

### Örnekler

Bir metin kutusu için iç kenar boşluklarının nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Belirli kenar boşluklarına sahip başka bir metin kutusu ekleyin.
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

Bir metin kutusu içindeki metnin yönünün nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 150, 100);
TextBox textBox = textBoxShape.TextBox;

// Belge oluşturucuyu TextBox'un içine taşıyın ve metin ekleyin.
builder.MoveTo(textBoxShape.LastParagraph);
builder.Writeln("Hello world!");
builder.Write("Hello again!");

// Bu metin kutusunun metin içeriğinin yönünü ayarlamak için "LayoutFlow" özelliğini ayarlayın.
textBox.LayoutFlow = layoutFlow;

doc.Save(ArtifactsDir + "Shape.TextBoxLayoutFlow.docx");
```

Bir metin kutusunun, içeriğine sıkı bir şekilde sığacak şekilde kendisini yeniden boyutlandırmasının nasıl sağlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 150, 100);
TextBox textBox = textBoxShape.TextBox;

// Ana şeklin sığması için bu değerleri her iki üyeye de uygulayın
// ayarladığımız boyutları göz ardı ederek metin içeriğinin etrafını sıkıca sarıyoruz.
textBox.FitShapeToText = true;
textBox.TextBoxWrapMode = TextBoxWrapMode.None;

builder.MoveTo(textBoxShape.LastParagraph);
builder.Write("Text fit tightly inside textbox.");

doc.Save(ArtifactsDir + "Shape.TextBoxFitShapeToText.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Drawing](../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../)


