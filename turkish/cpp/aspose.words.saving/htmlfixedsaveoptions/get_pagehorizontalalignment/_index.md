---
title: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_PageHorizontalAlignment metodu"
linktitle: "get_PageHorizontalAlignment"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_PageHorizontalAlignment metodu. HTML belgesindeki sayfaların yatay hizalamasını belirtir. Varsayılan değer C++'da Center'dır."
type: docs
weight: 12000
url: /tr/cpp/aspose.words.saving/htmlfixedsaveoptions/get_pagehorizontalalignment/
---
## HtmlFixedSaveOptions::get_PageHorizontalAlignment method


HTML belgesindeki sayfaların yatay hizalamasını belirtir. Varsayılan değer [Center](../../htmlfixedpagehorizontalalignment/).

```cpp
Aspose::Words::Saving::HtmlFixedPageHorizontalAlignment Aspose::Words::Saving::HtmlFixedSaveOptions::get_PageHorizontalAlignment() const
```


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

* Enum [HtmlFixedPageHorizontalAlignment](../../htmlfixedpagehorizontalalignment/)
* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
