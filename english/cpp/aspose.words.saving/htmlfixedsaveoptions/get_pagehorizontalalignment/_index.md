---
title: get_PageHorizontalAlignment
second_title: Aspose.Words for C++ API Reference
description: Specifies the horizontal alignment of pages in an HTML document. Default value is HtmlFixedHorizontalPageAlignment.Center.
type: docs
weight: 131
url: /cpp/aspose.words.saving/htmlfixedsaveoptions/get_pagehorizontalalignment/
---
## HtmlFixedSaveOptions.get_PageHorizontalAlignment method


Specifies the horizontal alignment of pages in an HTML document. Default value is **HtmlFixedHorizontalPageAlignment.Center**.

```cpp
Aspose::Words::Saving::HtmlFixedPageHorizontalAlignment Aspose::Words::Saving::HtmlFixedSaveOptions::get_PageHorizontalAlignment() const
```


## Examples




Shows how to set the horizontal alignment of pages when saving a document to HTML. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Rendering.docx");

auto htmlFixedSaveOptions = MakeObject<HtmlFixedSaveOptions>();
htmlFixedSaveOptions->set_PageHorizontalAlignment(pageHorizontalAlignment);

doc->Save(ArtifactsDir + u"HtmlFixedSaveOptions.HorizontalAlignment.html", htmlFixedSaveOptions);

String outDocContents = System::IO::File::ReadAllText(ArtifactsDir + u"HtmlFixedSaveOptions.HorizontalAlignment/styles.css");

switch (pageHorizontalAlignment)
{
case HtmlFixedPageHorizontalAlignment::Center:
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(
                    outDocContents, u"[.]awpage { position:relative; border:solid 1pt black; margin:10pt auto 10pt auto; overflow:hidden; }")
                    ->get_Success());
    break;

case HtmlFixedPageHorizontalAlignment::Left:
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(
                    outDocContents, u"[.]awpage { position:relative; border:solid 1pt black; margin:10pt auto 10pt 10pt; overflow:hidden; }")
                    ->get_Success());
    break;

case HtmlFixedPageHorizontalAlignment::Right:
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(
                    outDocContents, u"[.]awpage { position:relative; border:solid 1pt black; margin:10pt 10pt 10pt auto; overflow:hidden; }")
                    ->get_Success());
    break;
}
```

