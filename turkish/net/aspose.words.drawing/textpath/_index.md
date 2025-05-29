---
title: TextPath Class
linktitle: TextPath
articleTitle: TextPath
second_title: .NET için Aspose.Words
description: Çarpıcı WordArt'lar oluşturmak için Aspose.Words.Drawing.TextPath sınıfını keşfedin. Belgelerinizi geliştirmek için metni ve biçimlendirmeyi kolayca tanımlayın.
type: docs
weight: 1760
url: /tr/net/aspose.words.drawing/textpath/
---
## TextPath class

Metni ve metin yolunun (WordArt nesnesinin) biçimlendirmesini tanımlar.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Şekillerle Çalışma](https://docs.aspose.com/words/net/working-with-shapes/) belgeleme makalesi.

```csharp
public class TextPath
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Bold](../../aspose.words.drawing/textpath/bold/) { get; set; } | Yazı tipi kalın olarak biçimlendirilmişse doğrudur. |
| [FitPath](../../aspose.words.drawing/textpath/fitpath/) { get; set; } | Metnin bir şeklin yoluna uyup uymadığını tanımlar. |
| [FitShape](../../aspose.words.drawing/textpath/fitshape/) { get; set; } | Metnin bir şeklin sınırlayıcı kutusuna uyup uymadığını tanımlar. |
| [FontFamily](../../aspose.words.drawing/textpath/fontfamily/) { get; set; } | textpath yazı tipinin ailesini tanımlar. |
| [Italic](../../aspose.words.drawing/textpath/italic/) { get; set; } | Yazı tipi italik olarak biçimlendirilmişse doğrudur. |
| [Kerning](../../aspose.words.drawing/textpath/kerning/) { get; set; } | Kerning'in açık olup olmadığını belirler. |
| [On](../../aspose.words.drawing/textpath/on/) { get; set; } | Metnin görüntülenip görüntülenmeyeceğini tanımlar. |
| [ReverseRows](../../aspose.words.drawing/textpath/reverserows/) { get; set; } | Satırların düzen sırasının tersine çevrilip çevrilmeyeceğini belirler. |
| [RotateLetters](../../aspose.words.drawing/textpath/rotateletters/) { get; set; } | Metnin harflerinin döndürülüp döndürülmeyeceğini belirler. |
| [SameLetterHeights](../../aspose.words.drawing/textpath/sameletterheights/) { get; set; } | Tüm harflerin ilk harf durumundan bağımsız olarak aynı yükseklikte olup olmayacağını belirler. |
| [Shadow](../../aspose.words.drawing/textpath/shadow/) { get; set; } | Bir metin yolundaki metne gölge uygulanıp uygulanmayacağını tanımlar. |
| [Size](../../aspose.words.drawing/textpath/size/) { get; set; } | Yazı tipinin boyutunu nokta cinsinden tanımlar. |
| [SmallCaps](../../aspose.words.drawing/textpath/smallcaps/) { get; set; } | Yazı tipi küçük büyük harflerle biçimlendirilmişse doğrudur. |
| [Spacing](../../aspose.words.drawing/textpath/spacing/) { get; set; } | Metin için aralık miktarını tanımlar. 1, %100 anlamına gelir. |
| [StrikeThrough](../../aspose.words.drawing/textpath/strikethrough/) { get; set; } | Yazı tipi üstü çizili metin olarak biçimlendirilmişse doğrudur. |
| [Text](../../aspose.words.drawing/textpath/text/) { get; set; } | Metin yolunun metnini tanımlar. |
| [TextPathAlignment](../../aspose.words.drawing/textpath/textpathalignment/) { get; set; } | Metnin hizalamasını tanımlar. |
| [Trim](../../aspose.words.drawing/textpath/trim/) { get; set; } | Metnin üstünde ve altında bulunan fazladan boşluğun kaldırılıp kaldırılmayacağını belirler. |
| [Underline](../../aspose.words.drawing/textpath/underline/) { get; set; } | Yazı tipi altı çiziliyse doğrudur. |
| [XScale](../../aspose.words.drawing/textpath/xscale/) { get; set; } | Şekil yolu yerine düz bir metin yolunun kullanılıp kullanılmayacağını belirler. |

## Notlar

Kullanın[`TextPath`](../shape/textpath/) Bir şeklin WordArt özelliklerine erişmek için özellik. Örnekleri oluşturmazsınız`TextPath` sınıfa doğrudan.

## Örnekler

WordArt ile nasıl çalışılacağını gösterir.

```csharp
public void InsertTextPaths()
{
    Document doc = new Document();

    // Microsoft Word'de metni fareyi kullanarak yeniden boyutlandırabileceğimiz ve taşıyabileceğimiz bir şekil içerisinde görüntülemek için bir WordArt nesnesi ekleyin.
    // WordArt için bir şekil belirlemek amacıyla bir "ShapeType" argümanı sağlayın.
    Shape shape = AppendWordArt(doc, "Hello World! This text is bold, and italic.",
        "Arial", 480, 24, Color.White, Color.Black, ShapeType.TextPlainText);

    // Metne ilgili özellikleri kullanarak "Kalın" ve "İtalik" biçimlendirme ayarlarını uygulayın.
    shape.TextPath.Bold = true;
    shape.TextPath.Italic = true;

    // Aşağıda metin biçimlendirmeyle ilgili çeşitli diğer özellikler bulunmaktadır.
    Assert.False(shape.TextPath.Underline);
    Assert.False(shape.TextPath.Shadow);
    Assert.False(shape.TextPath.StrikeThrough);
    Assert.False(shape.TextPath.ReverseRows);
    Assert.False(shape.TextPath.XScale);
    Assert.False(shape.TextPath.Trim);
    Assert.False(shape.TextPath.SmallCaps);

    Assert.AreEqual(36.0, shape.TextPath.Size);
    Assert.AreEqual("Hello World! This text is bold, and italic.", shape.TextPath.Text);
    Assert.AreEqual(ShapeType.TextPlainText, shape.ShapeType);

    // Metni göstermek/gizlemek için "Açık" özelliğini kullanın.
    shape = AppendWordArt(doc, "On set to \"true\"", "Calibri", 150, 24, Color.Yellow, Color.Red, ShapeType.TextPlainText);
    shape.TextPath.On = true;

    shape = AppendWordArt(doc, "On set to \"false\"", "Calibri", 150, 24, Color.Yellow, Color.Purple, ShapeType.TextPlainText);
    shape.TextPath.On = false;

    // Belirli karakterler arasındaki aralık aralığını etkinleştirmek/devre dışı bırakmak için "Kerning" özelliğini kullanın.
    shape = AppendWordArt(doc, "Kerning: VAV", "Times New Roman", 90, 24, Color.Orange, Color.Red, ShapeType.TextPlainText);
    shape.TextPath.Kerning = true;

    shape = AppendWordArt(doc, "No kerning: VAV", "Times New Roman", 100, 24, Color.Orange, Color.Red, ShapeType.TextPlainText);
    shape.TextPath.Kerning = false;

    // Karakterler arasındaki özel aralığı 0,0 (hiçbiri) ile 1,0 (varsayılan) arasında bir ölçekte ayarlamak için "Boşluk" özelliğini kullanın.
    shape = AppendWordArt(doc, "Spacing set to 0.1", "Calibri", 120, 24, Color.BlueViolet, Color.Blue, ShapeType.TextCascadeDown);
    shape.TextPath.Spacing = 0.1;

    // Her karakteri saat yönünün tersine 90 derece döndürmek için "RotateLetters" özelliğini "true" olarak ayarlayın.
    shape = AppendWordArt(doc, "RotateLetters", "Calibri", 200, 36, Color.GreenYellow, Color.Green, ShapeType.TextWave);
    shape.TextPath.RotateLetters = true;

    // Her karakterin x yüksekliğinin büyük harf yüksekliğine eşit olması için "SameLetterHeights" özelliğini "true" olarak ayarlayın.
    shape = AppendWordArt(doc, "Same character height for lower and UPPER case", "Calibri", 300, 24, Color.DeepSkyBlue, Color.DodgerBlue, ShapeType.TextSlantUp);
    shape.TextPath.SameLetterHeights = true;

    // Varsayılan olarak, metnin boyutu her zaman içeren şeklin boyutuna uyacak şekilde ölçeklenir ve metin boyutu ayarı geçersiz kılınır.
    shape = AppendWordArt(doc, "FitShape on", "Calibri", 160, 24, Color.LightBlue, Color.Blue, ShapeType.TextPlainText);
    Assert.True(shape.TextPath.FitShape);
    shape.TextPath.Size = 24.0;

    // "FitShape: özelliğini "false" olarak ayarlarsak, metin boyutunu koruyacaktır
    // Şeklin boyutundan bağımsız olarak "Boyut" özelliğinin belirttiği değer.
    // Metni şeklin bir kenarına hizalamak için "TextPathAlignment" özelliğini de kullanın.
    shape = AppendWordArt(doc, "FitShape off", "Calibri", 160, 24, Color.LightBlue, Color.Blue, ShapeType.TextPlainText);
    shape.TextPath.FitShape = false;
    shape.TextPath.Size = 24.0;
    shape.TextPath.TextPathAlignment = TextPathAlignment.Right;

    doc.Save(ArtifactsDir + "Shape.InsertTextPaths.docx");
}

/// <summary>
/// İçinde WordArt şekli bulunan yeni bir paragraf ekle.
/// </summary>
private static Shape AppendWordArt(Document doc, string text, string textFontFamily, double shapeWidth, double shapeHeight, Color wordArtFill, Color line, ShapeType wordArtShapeType)
{
    // WordArt'ımız için bir kapsayıcı görevi görecek satır içi bir Şekil oluşturun.
    // Şekle, yalnızca WordArt tarafından belirlenmiş bir Şekil Türü atarsak geçerli bir WordArt şekli olabilir.
    // Bu türlerin açıklamasında "WordArt nesnesi" bulunacaktır.
    // ve bunların numaralandırıcı sabit isimlerinin hepsi "Text" ile başlayacaktır.
    Shape shape = new Shape(doc, wordArtShapeType)
    {
        WrapType = WrapType.Inline,
        Width = shapeWidth,
        Height = shapeHeight,
        FillColor = wordArtFill,
        StrokeColor = line
    };

    shape.TextPath.Text = text;
    shape.TextPath.FontFamily = textFontFamily;

    Paragraph para = (Paragraph)doc.FirstSection.Body.AppendChild(new Paragraph(doc));
    para.AppendChild(shape);
    return shape;
}
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Drawing](../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../)
