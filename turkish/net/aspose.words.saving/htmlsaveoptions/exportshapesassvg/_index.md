---
title: HtmlSaveOptions.ExportShapesAsSvg
second_title: Aspose.Words for .NET API Referansı
description: HtmlSaveOptions mülk. olup olmadığını kontrol ederShapedüğümler yi HTML MHTML EPUB veya AZW3e kaydederken SVG görüntülerine dönüştürülür. Varsayılan değerYANLIŞ .
type: docs
weight: 250
url: /tr/net/aspose.words.saving/htmlsaveoptions/exportshapesassvg/
---
## HtmlSaveOptions.ExportShapesAsSvg property

olup olmadığını kontrol eder[`Shape`](../../../aspose.words.drawing/shape/)düğümler 'yi HTML, MHTML, EPUB veya AZW3'e kaydederken SVG görüntülerine dönüştürülür. Varsayılan değer:`YANLIŞ` .

```csharp
public bool ExportShapesAsSvg { get; set; }
```

### Notlar

Bu seçenek şu şekilde ayarlanırsa`doğru` ,[`Shape`](../../../aspose.words.drawing/shape/) düğümler &lt;svg&gt; öğeleri olarak dışa aktarılır. Aksi takdirde, bitmaplere dönüştürülür ve &lt;img&gt; öğeleri olarak dışa aktarılır.

### Örnekler

Şeklin ölçeklenebilir vektör grafikleri olarak nasıl dışa aktarılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBox = builder.InsertShape(ShapeType.TextBox, 100.0, 60.0);
builder.MoveTo(textBox.FirstParagraph);
builder.Write("My text box");

// Belgeyi HTML'ye kaydettiğimizde SaveOptions nesnesini iletebiliriz
// kaydetme işleminin metin kutusu şekillerini nasıl dışa aktaracağını belirlemek için.
// "ExportTextBoxAsSvg" flagını "true" olarak ayarlarsak,
// kaydetme işlemi metin içeren şekilleri SVG nesnelerine dönüştürecektir.
// "ExportTextBoxAsSvg" flagını "false" olarak ayarlarsak,
// kaydetme işlemi metin içeren şekilleri görsellere dönüştürecektir.
HtmlSaveOptions options = new HtmlSaveOptions { ExportShapesAsSvg = exportShapesAsSvg };

doc.Save(ArtifactsDir + "HtmlSaveOptions.ExportTextBox.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ExportTextBox.html");

if (exportShapesAsSvg)
{
    Assert.True(outDocContents.Contains(
        "<span style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\">" +
        "<svg xmlns=\"http://www.w3.org/2000/svg\" xmlns:xlink=\"http://www.w3.org/1999/xlink\" version=\"1.1\" width=\"133\" height= \"80\">"));
}
else
{
    Assert.True(outDocContents.Contains(
        "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
            "<img src=\"HtmlSaveOptions.ExportTextBox.001.png\" width=\"136\" height=\"83\" alt=\"\" " +
            "style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\" />" +
        "</p>"));
}
```

### Ayrıca bakınız

* class [HtmlSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../htmlsaveoptions/)
* toplantı [Aspose.Words](../../../)


