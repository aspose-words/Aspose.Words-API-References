---
title: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedSvg 方法"
linktitle: "get_ExportEmbeddedSvg"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedSvg 方法。指定是否应将 SVG 资源嵌入到 Html 文档中。默认在 C++ 中为 true。"
type: docs
weight: 8000
url: /zh/cpp/aspose.words.saving/htmlfixedsaveoptions/get_exportembeddedsvg/
---
## HtmlFixedSaveOptions::get_ExportEmbeddedSvg method


指定是否应将 SVG 资源嵌入 Html 文档。默认值为 **true**。

```cpp
bool Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedSvg() const
```


## 示例



展示了在将文档导出为 Html 时如何确定 SVG 对象的存储位置。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");

// 当我们将包含 SVG 对象的文档导出为 .html 时，
// Aspose.Words 可以将这些对象放置在两种可能的位置。
// 将 "ExportEmbeddedSvg" 标志设置为 "true" 将嵌入所有 SVG 对象的原始数据
// 在输出的 HTML 中，位于 <image> 标签内部。
// 将此标志设置为 "false" 将为每个 SVG 对象在本地文件系统中创建一个文件。
// HTML 将使用 <object> 标签的 "data" 属性链接到每个文件。
auto htmlFixedSaveOptions = System::MakeObject<Aspose::Words::Saving::HtmlFixedSaveOptions>();
htmlFixedSaveOptions->set_ExportEmbeddedSvg(exportSvgs);

doc->Save(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedSvgs.html", htmlFixedSaveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedSvgs.html");

if (exportSvgs)
{
    ASSERT_FALSE(System::IO::File::Exists(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedSvgs/svg001.svg"));
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, u"<image id=\"image004\" xlink:href=.+/>")->get_Success());
}
else
{
    ASSERT_TRUE(System::IO::File::Exists(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedSvgs/svg001.svg"));
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, u"<object type=\"image/svg[+]xml\" data=\"HtmlFixedSaveOptions.ExportEmbeddedSvgs/svg001[.]svg\"></object>")->get_Success());
}
```

## 另见

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
