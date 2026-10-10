---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_CssClassNamePrefix 方法"
linktitle: "get_CssClassNamePrefix"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_CssClassNamePrefix 方法。指定添加到所有 CSS 类名的前缀。默认值在 C++ 中为空字符串，生成的 CSS 类名没有公共前缀。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words.saving/htmlsaveoptions/get_cssclassnameprefix/
---
## HtmlSaveOptions::get_CssClassNamePrefix method


指定添加到所有 CSS 类名的前缀。默认值为空字符串，生成的 CSS 类名没有公共前缀。

```cpp
System::String Aspose::Words::Saving::HtmlSaveOptions::get_CssClassNamePrefix() const
```

## 备注


如果此值不为空，Aspose.Words 生成的所有 CSS 类都会以指定的前缀开头。例如，当您向生成的文档添加自定义 CSS 并希望避免类名冲突时，这可能会很有用。

如果该值不是 **null** 或为空，则必须是有效的 CSS 标识符。

## 示例



展示如何将文档保存为 HTML，并为其所有 CSS 类名添加前缀。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Paragraphs.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
saveOptions->set_CssStyleSheetType(Aspose::Words::Saving::CssStyleSheetType::External);
saveOptions->set_CssClassNamePrefix(u"myprefix-");

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.CssClassNamePrefix.html", saveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.CssClassNamePrefix.html");

ASSERT_TRUE(outDocContents.Contains(u"<p class=\"myprefix-Header\">"));
ASSERT_TRUE(outDocContents.Contains(u"<p class=\"myprefix-Footer\">"));

outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.CssClassNamePrefix.css");

ASSERT_TRUE(outDocContents.Contains(u".myprefix-Footer { margin-bottom:0pt; line-height:normal; font-family:Arial; font-size:11pt; -aw-style-name:footer }"));
ASSERT_TRUE(outDocContents.Contains(u".myprefix-Header { margin-bottom:0pt; line-height:normal; font-family:Arial; font-size:11pt; -aw-style-name:header }"));
```

## 另见

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
