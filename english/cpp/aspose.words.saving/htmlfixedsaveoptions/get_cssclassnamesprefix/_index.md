---
title: get_CssClassNamesPrefix
second_title: Aspose.Words for C++ API Reference
description: Specifies prefix which is added to all class names in style.css file. Default value is %"aw".
type: docs
weight: 14
url: /cpp/aspose.words.saving/htmlfixedsaveoptions/get_cssclassnamesprefix/
---
## HtmlFixedSaveOptions::get_CssClassNamesPrefix method


Specifies prefix which is added to all class names in style.css file. Default value is **%"aw"**.

```cpp
System::String Aspose::Words::Saving::HtmlFixedSaveOptions::get_CssClassNamesPrefix() const
```


## Examples



Shows how to place CSS into a separate file and add a prefix to all of its CSS class names. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Bookmarks.docx");

auto htmlFixedSaveOptions = MakeObject<HtmlFixedSaveOptions>();
htmlFixedSaveOptions->set_CssClassNamesPrefix(u"myprefix");
htmlFixedSaveOptions->set_SaveFontFaceCssSeparately(true);

doc->Save(ArtifactsDir + u"HtmlFixedSaveOptions.AddCssClassNamesPrefix.html", htmlFixedSaveOptions);

String outDocContents = System::IO::File::ReadAllText(ArtifactsDir + u"HtmlFixedSaveOptions.AddCssClassNamesPrefix.html");

ASSERT_TRUE(
    System::Text::RegularExpressions::Regex::Match(
        outDocContents, String(u"<div class=\"myprefixdiv myprefixpage\" style=\"width:595[.]3pt; height:841[.]9pt;\">") +
                            u"<div class=\"myprefixdiv\" style=\"left:85[.]05pt; top:36pt; clip:rect[(]0pt,510[.]25pt,74[.]95pt,-85.05pt[)];\">" +
                            u"<span class=\"myprefixspan myprefixtext001\" style=\"font-size:11pt; left:294[.]73pt; top:0[.]36pt; line-height:12[.]29pt;\">")
        ->get_Success());

outDocContents = System::IO::File::ReadAllText(ArtifactsDir + u"HtmlFixedSaveOptions.AddCssClassNamesPrefix/styles.css");

ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents,
                                                           String(u".myprefixdiv { position:absolute; } ") +
                                                               u".myprefixspan { position:absolute; white-space:pre; color:#000000; font-size:12pt; }")
                ->get_Success());
```

## See Also

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)
