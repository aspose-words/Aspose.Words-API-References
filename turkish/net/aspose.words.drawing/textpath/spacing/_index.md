---
title: TextPath.Spacing
second_title: Aspose.Words for .NET API Referansı
description: TextPath mülk. Metin için boşluk miktarını tanımlar. 1 100 anlamına gelir.
type: docs
weight: 140
url: /tr/net/aspose.words.drawing/textpath/spacing/
---
## TextPath.Spacing property

Metin için boşluk miktarını tanımlar. 1, %100 anlamına gelir.

```csharp
public double Spacing { get; set; }
```

### Notlar

Varsayılan değer 1'dir.

### Örnekler

WordArt ile nasıl çalışılacağını gösterir.

```csharp
{
    Document doc = new Document();

    // Metni Microsoft Word'de fareyi kullanarak yeniden boyutlandırabileceğimiz ve taşıyabileceğimiz bir şekilde görüntülemek için bir WordArt nesnesi ekleyin.
    // WordArt için bir şekil ayarlamak için argüman olarak bir "ShapeType" sağlayın.
    Shape shape = AppendWordArt(doc, "Hello World! This text is bold, and italic.", 
        "Arial", 480, 24, Color.White, Color.Black, ShapeType.TextPlainText);

    // İlgili özellikleri kullanarak metne "Kalın" ve "İtalik" biçimlendirme ayarlarını uygulayın.
    shape.TextPath.Bold = true;
    shape.TextPath.Italic = true;

    // Aşağıda, metin biçimlendirme ile ilgili diğer çeşitli özellikler bulunmaktadır.
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

    // Metni göstermek/gizlemek için "On" özelliğini kullanın.
    shape = AppendWordArt(doc, "On set to \"true\"", "Calibri", 150, 24, Color.Yellow, Color.Red, ShapeType.TextPlainText);
    shape.TextPath.On = true;

    shape = AppendWordArt(doc, "On set to \"false\"", "Calibri", 150, 24, Color.Yellow, Color.Purple, ShapeType.TextPlainText);
    shape.TextPath.On = false;

    // Belirli karakterler arasındaki karakter aralığı aralığını etkinleştirmek/devre dışı bırakmak için "Kerning" özelliğini kullanın.
    shape = AppendWordArt(doc, "Kerning: VAV", "Times New Roman", 90, 24, Color.Orange, Color.Red, ShapeType.TextPlainText);
    shape.TextPath.Kerning = true;

    shape = AppendWordArt(doc, "No kerning: VAV", "Times New Roman", 100, 24, Color.Orange, Color.Red, ShapeType.TextPlainText);
    shape.TextPath.Kerning = false;

    // Karakterler arasındaki özel aralığı 0,0 (yok) ile 1,0 (varsayılan) arasında ayarlamak için "Spacing" özelliğini kullanın.
    shape = AppendWordArt(doc, "Spacing set to 0.1", "Calibri", 120, 24, Color.BlueViolet, Color.Blue, ShapeType.TextCascadeDown);
    shape.TextPath.Spacing = 0.1;

    // Her karakteri saat yönünün tersine 90 derece döndürmek için "RotateLetters" özelliğini "true" olarak ayarlayın.
    shape = AppendWordArt(doc, "RotateLetters", "Calibri", 200, 36, Color.GreenYellow, Color.Green, ShapeType.TextWave);
    shape.TextPath.RotateLetters = true;

    // Her karakterin x-yüksekliğini başlık yüksekliğine eşitlemek için "SameLetterHeights" özelliğini "true" olarak ayarlayın.
    shape = AppendWordArt(doc, "Same character height for lower and UPPER case", "Calibri", 300, 24, Color.DeepSkyBlue, Color.DodgerBlue, ShapeType.TextSlantUp);
    shape.TextPath.SameLetterHeights = true;

    // Varsayılan olarak, metnin boyutu, metin boyutu ayarını geçersiz kılarak, her zaman içerdiği şeklin boyutuna uyacak şekilde ölçeklenir.
    shape = AppendWordArt(doc, "FitShape on", "Calibri", 160, 24, Color.LightBlue, Color.Blue, ShapeType.TextPlainText);
    Assert.True(shape.TextPath.FitShape);
    shape.TextPath.Size = 24.0;

    // "FitShape: özelliğini "false" olarak ayarlarsak, metin boyutu koruyacaktır
    // şeklin boyutundan bağımsız olarak "Size" özelliğinin belirttiği.
    // Metni şeklin bir kenarına hizalamak için de "TextPathAlignment" özelliğini kullanın.
    shape = AppendWordArt(doc, "FitShape off", "Calibri", 160, 24, Color.LightBlue, Color.Blue, ShapeType.TextPlainText);
    shape.TextPath.FitShape = false;
    shape.TextPath.Size = 24.0;
    shape.TextPath.TextPathAlignment = TextPathAlignment.Right;

    doc.Save(ArtifactsDir + "Shape.InsertTextPaths.docx");

/// <summary>
/// İçinde WordArt şekli olan yeni bir paragraf ekleyin.
/// </summary>
private static Shape AppendWordArt(Document doc, string text, string textFontFamily, double shapeWidth, double shapeHeight, Color wordArtFill, Color line, ShapeType wordArtShapeType)
{
    // WordArt'ımız için bir kapsayıcı görevi görecek bir satır içi Şekil oluşturun.
    // Şekil, yalnızca ona WordArt tarafından atanan bir ShapeType atadığımızda geçerli bir WordArt şekli olabilir.
    // Bu türlerin açıklamasında "WordArt nesnesi" olacaktır,
    // ve numaralandırıcı sabit adlarının tümü "Metin" ile başlayacak.
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

* class [TextPath](../)
* ad alanı [Aspose.Words.Drawing](../../textpath/)
* toplantı [Aspose.Words](../../../)


