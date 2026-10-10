---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportShapesAsSvg metodu"
linktitle: "get_ExportShapesAsSvg"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportShapesAsSvg metodu. Shape düğümlerinin HTML, MHTML, EPUB veya AZW3 olarak kaydedilirken SVG görüntülerine dönüştürülüp dönüştürülmeyeceğini kontrol eder. Varsayılan değer C++'da false'tur."
type: docs
weight: 27000
url: /tr/cpp/aspose.words.saving/htmlsaveoptions/get_exportshapesassvg/
---
## HtmlSaveOptions::get_ExportShapesAsSvg method


HTML, MHTML, EPUB veya AZW3 olarak kaydedilirken [Shape](../../../aspose.words.drawing/shape/) düğümlerinin SVG görüntülerine dönüştürülüp dönüştürülmeyeceğini kontrol eder. Varsayılan değer **false**'dır.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportShapesAsSvg() const
```

## Açıklamalar


Bu seçenek **true** olarak ayarlanırsa, [Shape](../../../aspose.words.drawing/shape/) düğümleri <svg> öğeleri olarak dışa aktarılır. Aksi takdirde, bitmap olarak işlenir ve <img> öğeleri olarak dışa aktarılır.

## Örnekler



Şekli ölçeklenebilir vektör grafiği olarak dışa aktarmanın nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> textBox = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 100.0, 60.0);
builder->MoveTo(textBox->get_FirstParagraph());
builder->Write(u"My text box");

// Belgeyi HTML olarak kaydettiğimizde, bir SaveOptions nesnesi geçebiliriz.
// kaydetme işleminin metin kutusu şekillerini nasıl dışa aktaracağını belirlemek için.
// Eğer "ExportTextBoxAsSvg" bayrağını "true" olarak ayarlarsak,
// kaydetme işlemi, metin içeren şekilleri SVG nesnelerine dönüştürecektir.
// Eğer "ExportTextBoxAsSvg" bayrağını "false" olarak ayarlarsak,
// kaydetme işlemi, metin içeren şekilleri görüntülere dönüştürecektir.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportShapesAsSvg(exportShapesAsSvg);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ExportTextBox.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.ExportTextBox.html");

if (exportShapesAsSvg)
{
    ASSERT_TRUE(outDocContents.Contains(System::String(u"<span style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\">") + u"<svg xmlns=\"http://www.w3.org/2000/svg\" xmlns:xlink=\"http://www.w3.org/1999/xlink\" version=\"1.1\" width=\"133\" height=\"80\">"));
}
else
{
    ASSERT_TRUE(outDocContents.Contains(System::String(u"<p style=\"margin-top:0pt; margin-bottom:0pt\">") + u"<img src=\"HtmlSaveOptions.ExportTextBox.001.png\" width=\"136\" height=\"83\" alt=\"\" " + u"style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\" />" + u"</p>"));
}
```

## Ayrıca Bakınız

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
