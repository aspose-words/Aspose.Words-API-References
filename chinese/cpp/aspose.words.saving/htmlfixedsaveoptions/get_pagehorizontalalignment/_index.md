---
title: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_PageHorizontalAlignment 方法"
linktitle: "get_PageHorizontalAlignment"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_PageHorizontalAlignment 方法。指定 HTML 文档中页面的水平对齐方式。默认值在 C++ 中为 Center。"
type: docs
weight: 12000
url: /zh/cpp/aspose.words.saving/htmlfixedsaveoptions/get_pagehorizontalalignment/
---
## HtmlFixedSaveOptions::get_PageHorizontalAlignment method


指定 HTML 文档中页面的水平对齐方式。默认值为 [Center](../../htmlfixedpagehorizontalalignment/)。

```cpp
Aspose::Words::Saving::HtmlFixedPageHorizontalAlignment Aspose::Words::Saving::HtmlFixedSaveOptions::get_PageHorizontalAlignment() const
```


## 示例



展示如何在将文档保存为 HTML 时设置页面的水平对齐。
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

## 另见

* Enum [HtmlFixedPageHorizontalAlignment](../../htmlfixedpagehorizontalalignment/)
* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
