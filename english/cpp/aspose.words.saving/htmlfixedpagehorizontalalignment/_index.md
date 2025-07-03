---
title: Aspose::Words::Saving::HtmlFixedPageHorizontalAlignment enum
linktitle: HtmlFixedPageHorizontalAlignment
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::HtmlFixedPageHorizontalAlignment enum. Specifies the horizontal alignment for pages in output HTML document in C++.'
type: docs
weight: 59000
url: /cpp/aspose.words.saving/htmlfixedpagehorizontalalignment/
---
## HtmlFixedPageHorizontalAlignment enum


Specifies the horizontal alignment for pages in output HTML document.

```cpp
enum class HtmlFixedPageHorizontalAlignment
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Left | 0 | Align pages to the left. |
| Center | 1 | Center pages. This is the default value. |
| Right | 2 | Align pages to the right. |


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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
