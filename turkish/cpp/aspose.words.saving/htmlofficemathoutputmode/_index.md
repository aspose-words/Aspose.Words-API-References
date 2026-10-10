---
title: "Aspose::Words::Saving::HtmlOfficeMathOutputMode enum"
linktitle: "HtmlOfficeMathOutputMode"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::HtmlOfficeMathOutputMode enum. Aspose.Words, OfficeMath'i HTML, MHTML ve EPUB'e C++ içinde nasıl dışa aktardığını belirtir."
type: docs
weight: 61000
url: /tr/cpp/aspose.words.saving/htmlofficemathoutputmode/
---
## HtmlOfficeMathOutputMode enum


Aspose.Words'in OfficeMath'i HTML, MHTML ve EPUB formatına nasıl dışa aktardığını belirtir.

```cpp
enum class HtmlOfficeMathOutputMode
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| Image | 0 | OfficeMath, <img> etiketiyle belirtilen bir görüntü olarak HTML'ye dönüştürülür. |
| MathML | 1 | OfficeMath, MathML kullanılarak HTML'ye dönüştürülür. |
| Metin | 2 | OfficeMath, <span> etiketleriyle belirtilen bir dizi koşul (run) olarak HTML'ye dönüştürülür. |


## Örnekler



Microsoft OfficeMath nesnelerinin HTML'ye nasıl dışa aktarılacağını belirtmenin bir örneğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

// Belgeyi HTML olarak kaydettiğimizde, bir SaveOptions nesnesi geçebiliriz.
// Kaydetme işleminin OfficeMath nesnelerini nasıl ele aldığını belirlemek için.
// \"OfficeMathOutputMode\" özelliğini \"HtmlOfficeMathOutputMode.Image\" olarak ayarlama
// her OfficeMath nesnesini bir görüntüye render eder.
// \"OfficeMathOutputMode\" özelliğini \"HtmlOfficeMathOutputMode.MathML\" olarak ayarlama
// her OfficeMath nesnesini MathML'e dönüştürür.
// \"OfficeMathOutputMode\" özelliğini \"HtmlOfficeMathOutputMode.Text\" olarak ayarlama
// her OfficeMath formülünü düz HTML metni kullanarak temsil eder.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_OfficeMathOutputMode(htmlOfficeMathOutputMode);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.OfficeMathOutputMode.html", options);
System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.OfficeMathOutputMode.html");

switch (htmlOfficeMathOutputMode)
{
    case Aspose::Words::Saving::HtmlOfficeMathOutputMode::Image:
        ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, System::String(u"<p style=\"margin-top:0pt; margin-bottom:10pt\">") + u"<img src=\"HtmlSaveOptions.OfficeMathOutputMode.001.png\" width=\"163\" height=\"19\" alt=\"\" style=\"vertical-align:middle; " + u"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\" />" + u"</p>")->get_Success());
        break;

    case Aspose::Words::Saving::HtmlOfficeMathOutputMode::MathML:
        ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, System::String(u"<p style=\"margin-top:0pt; margin-bottom:10pt; text-align:center\">") + u"<math xmlns=\"http://www.w3.org/1998/Math/MathML\">" + u"<mi>i</mi>" + u"<mo>[+]</mo>" + u"<mi>b</mi>" + u"<mo>-</mo>" + u"<mi>c</mi>" + u"<mo>≥</mo>" + u".*" + u"</math>" + u"</p>")->get_Success());
        break;

    case Aspose::Words::Saving::HtmlOfficeMathOutputMode::Text:
        ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, System::String(u"<p style=\\\"margin-top:0pt; margin-bottom:10pt; text-align:center\\\">") + u"<span style=\\\"font-family:'Cambria Math'\\\">i[+]b-c≥iM[+]bM-cM </span>" + u"</p>")->get_Success());
        break;

}
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
