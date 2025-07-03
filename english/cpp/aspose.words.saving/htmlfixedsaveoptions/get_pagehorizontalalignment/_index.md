---
title: Aspose::Words::Saving::HtmlFixedSaveOptions::get_PageHorizontalAlignment method
linktitle: get_PageHorizontalAlignment
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::HtmlFixedSaveOptions::get_PageHorizontalAlignment method. Specifies the horizontal alignment of pages in an HTML document. Default value is Center in C++.'
type: docs
weight: 12000
url: /cpp/aspose.words.saving/htmlfixedsaveoptions/get_pagehorizontalalignment/
---
## HtmlFixedSaveOptions::get_PageHorizontalAlignment method


Specifies the horizontal alignment of pages in an HTML document. Default value is [Center](../../htmlfixedpagehorizontalalignment/).

```cpp
Aspose::Words::Saving::HtmlFixedPageHorizontalAlignment Aspose::Words::Saving::HtmlFixedSaveOptions::get_PageHorizontalAlignment() const
```


## Examples



Shows how to set the horizontal alignment of pages when saving a document to HTML. 
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

## See Also

* Enum [HtmlFixedPageHorizontalAlignment](../../htmlfixedpagehorizontalalignment/)
* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
