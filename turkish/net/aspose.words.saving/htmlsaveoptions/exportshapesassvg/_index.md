---
title: HtmlSaveOptions.ExportShapesAsSvg
linktitle: ExportShapesAsSvg
articleTitle: ExportShapesAsSvg
second_title: .NET için Aspose.Words
description: HtmlSaveOptions ExportShapesAsSvg'yi kullanarak HTML, MHTML, EPUB veya AZW3 formatlarında kaydederken Şekil düğümlerini SVG görüntülerine nasıl dönüştüreceğinizi keşfedin.
type: docs
weight: 250
url: /tr/net/aspose.words.saving/htmlsaveoptions/exportshapesassvg/
---
## HtmlSaveOptions.ExportShapesAsSvg property

Kontroller[`Shape`](../../../aspose.words.drawing/shape/)düğümler, saving HTML, MHTML, EPUB veya AZW3'e dönüştürüldüğünde SVG görüntülerine dönüştürülür. Varsayılan değer`YANLIŞ` .

```csharp
public bool ExportShapesAsSvg { get; set; }
```

## Notlar

Bu seçenek şu şekilde ayarlanırsa`doğru` ,[`Shape`](../../../aspose.words.drawing/shape/) düğümler &lt;svg&gt; öğeleri olarak dışa aktarılır. Aksi takdirde, bit eşlemlere dönüştürülür ve &lt;img&gt; öğeleri olarak dışa aktarılır.

## Örnekler

Şeklin ölçeklenebilir vektör grafikleri olarak nasıl dışa aktarılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBox = builder.InsertShape(ShapeType.TextBox, 100.0, 60.0);
builder.MoveTo(textBox.FirstParagraph);
builder.Write("My text box");

// Belgeyi HTML'e kaydettiğimizde, SaveOptions nesnesini geçirebiliriz
// kaydetme işleminin metin kutusu şekillerini nasıl dışa aktaracağını belirlemek için.
// "ExportTextBoxAsSvg" bayrağını "true" olarak ayarlarsak,
// Kaydetme işlemi metin içeren şekilleri SVG nesnelerine dönüştürecektir.
// "ExportTextBoxAsSvg" bayrağını "false" olarak ayarlarsak,
// Kaydetme işlemi metin içeren şekilleri resimlere dönüştürecektir.
HtmlSaveOptions options = new HtmlSaveOptions { ExportShapesAsSvg = exportShapesAsSvg };

doc.Save(ArtifactsDir + "HtmlSaveOptions.ExportTextBox.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ExportTextBox.html");

if (exportShapesAsSvg)
{
    Assert.True(outDocContents.Contains(
        "<span style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\">" +
        "<svg xmlns=\"http://www.w3.org/2000/svg\" xmlns:xlink=\"http://www.w3.org/1999/xlink\" sürüm=\"1.1\" genişlik=\"133\" yükseklik=\"80\">"));
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
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
