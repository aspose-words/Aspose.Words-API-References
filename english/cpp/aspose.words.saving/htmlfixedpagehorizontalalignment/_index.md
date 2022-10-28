---
title: HtmlFixedPageHorizontalAlignment
second_title: Aspose.Words for C++ API Reference
description: Specifies the horizontal alignment for pages in output HTML document.
type: docs
weight: 755
url: /cpp/aspose.words.saving/htmlfixedpagehorizontalalignment/
---
## HtmlFixedPageHorizontalAlignment enum


Specifies the horizontal alignment for pages in output HTML document.

### Values

| Name | Value | Description |
| --- | --- | --- |
| Left | 0 | Align pages to the left. |
| Center | 1 | Center pages. This is the default value. |
| Right | 2 | Align pages to the right. |


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

