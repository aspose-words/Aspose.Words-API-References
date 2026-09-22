---
title: "Aspose::Words::Saving::HtmlFixedPageHorizontalAlignment enum"
linktitle: "HtmlFixedPageHorizontalAlignment"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::HtmlFixedPageHorizontalAlignment enum. C++'ta çıktı HTML belgesindeki sayfalar için yatay hizalamayı belirtir."
type: docs
weight: 59000
url: /tr/cpp/aspose.words.saving/htmlfixedpagehorizontalalignment/
---
## HtmlFixedPageHorizontalAlignment enum


Çıktı HTML belgesindeki sayfalar için yatay hizalamayı belirtir.

```cpp
enum class HtmlFixedPageHorizontalAlignment
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| Sol | 0 | Sayfaları sola hizala. |
| Orta | 1 | Sayfaları ortala. Bu varsayılan değerdir. |
| Sağ | 2 | Sayfaları sağa hizala. |


## Örnekler



Bir belgeyi HTML olarak kaydederken sayfaların yatı hizalamasını nasıl ayarlayacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto htmlFixedSaveOptions = System::MakeObject<Aspose::Words::Saving::HtmlFixedSaveOptions>();
htmlFixedSaveOptions->set_PageHorizontalAlignment(pageHorizontalAlignment);

doc->Save(get_ArtifactsDir() + u"HtmlFixedSaveOptions.HorizontalAlignment.html", htmlFixedSaveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlFixedSaveOptions.HorizontalAlignment/styles.css");

switch (pageHorizontalAlignment)
{
    case Aspose::Words::Saving::HtmlFixedPageHorizontalAlignment::Center:
        ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, u"[.]awpage { position:relative; border:solid 1pt black; margin:10pt auto 10pt auto; overflow:hidden; }")->get_Success());
        break;

    case Aspose::Words::Saving::HtmlFixedPageHorizontalAlignment::Left:
        ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, u"[.]awpage { position:relative; border:solid 1pt black; margin:10pt auto 10pt 10pt; overflow:hidden; }")->get_Success());
        break;

    case Aspose::Words::Saving::HtmlFixedPageHorizontalAlignment::Right:
        ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, u"[.]awpage { position:relative; border:solid 1pt black; margin:10pt 10pt 10pt auto; overflow:hidden; }")->get_Success());
        break;

}
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
