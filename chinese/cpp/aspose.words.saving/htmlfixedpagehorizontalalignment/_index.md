---
title: "Aspose::Words::Saving::HtmlFixedPageHorizontalAlignment 枚举"
linktitle: "HtmlFixedPageHorizontalAlignment"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::HtmlFixedPageHorizontalAlignment 枚举。指定 C++ 中输出 HTML 文档页面的水平对齐方式。"
type: docs
weight: 59000
url: /zh/cpp/aspose.words.saving/htmlfixedpagehorizontalalignment/
---
## HtmlFixedPageHorizontalAlignment enum


指定输出 HTML 文档中页面的水平对齐方式。

```cpp
enum class HtmlFixedPageHorizontalAlignment
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| 左 | 0 | 将页面左对齐。 |
| 居中 | 1 | 页面居中。这是默认值。 |
| 右 | 2 | 将页面右对齐。 |


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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
