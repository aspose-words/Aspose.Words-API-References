---
title: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedCss 方法"
linktitle: "get_ExportEmbeddedCss"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedCss 方法。指定是否应在 C++ 中将 CSS（层叠样式表）嵌入到 Html 文档中。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words.saving/htmlfixedsaveoptions/get_exportembeddedcss/
---
## HtmlFixedSaveOptions::get_ExportEmbeddedCss method


指定是否应将 CSS（层叠[Style](../../../aspose.words/style/) 表）嵌入到 Html 文档中。

```cpp
bool Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedCss() const
```


## 示例



展示如何在将文档导出为 Html 时确定 CSS 样式表的存储位置。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// 当我们将文档导出为 html 时，Aspose.Words 还会创建一个 CSS 样式表来格式化文档。
// 将 "ExportEmbeddedCss" 标志设置为 "true" 时，会将 CSS 样式表保存为 .css 文件，
// 并使用 <link> 元素在 html 文档中链接到该文件。
// 将标志设置为 "false" 时，会将 CSS 样式表嵌入到 Html 文档中，
// 这样只会生成一个文件，而不是两个。
auto htmlFixedSaveOptions = System::MakeObject<Aspose::Words::Saving::HtmlFixedSaveOptions>();
htmlFixedSaveOptions->set_ExportEmbeddedCss(exportEmbeddedCss);

doc->Save(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedCss.html", htmlFixedSaveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedCss.html");

if (exportEmbeddedCss)
{
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, u"<style type=\"text/css\">")->get_Success());
    ASSERT_FALSE(System::IO::File::Exists(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedCss/styles.css"));
}
else
{
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, u"<link rel=\"stylesheet\" type=\"text/css\" href=\"HtmlFixedSaveOptions[.]ExportEmbeddedCss/styles[.]css\" media=\"all\" />")->get_Success());
    ASSERT_TRUE(System::IO::File::Exists(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedCss/styles.css"));
}
```

## 另见

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
