---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_OfficeMathOutputMode yöntemi"
linktitle: "get_OfficeMathOutputMode"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_OfficeMathOutputMode yöntemi. OfficeMath nesnelerinin HTML, MHTML veya EPUB'a nasıl dışa aktarıldığını kontrol eder. Varsayılan değer C++'da Image'dir."
type: docs
weight: 41000
url: /tr/cpp/aspose.words.saving/htmlsaveoptions/get_officemathoutputmode/
---
## HtmlSaveOptions::get_OfficeMathOutputMode method


OfficeMath nesnelerinin HTML, MHTML veya EPUB'a nasıl dışa aktarıldığını kontrol eder. Varsayılan değer [Image](../../htmlofficemathoutputmode/)‘dır.

```cpp
Aspose::Words::Saving::HtmlOfficeMathOutputMode Aspose::Words::Saving::HtmlSaveOptions::get_OfficeMathOutputMode() const
```


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

* Enum [HtmlOfficeMathOutputMode](../../htmlofficemathoutputmode/)
* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
