---
title: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedFonts method"
linktitle: "get_ExportEmbeddedFonts"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedFonts 方法。指定是否应以 Base64 格式将字体嵌入到 Html 文档中。注意，设置此标志可能会显著增加 C++ 中输出 Html 文件的大小。"
type: docs
weight: 6000
url: /zh/cpp/aspose.words.saving/htmlfixedsaveoptions/get_exportembeddedfonts/
---
## HtmlFixedSaveOptions::get_ExportEmbeddedFonts method


指定是否应以 Base64 格式将字体嵌入 Html 文档。请注意，设置此标志可能会显著增加输出 Html 文件的大小。

```cpp
bool Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedFonts() const
```


## 示例



展示如何在将文档导出为 Html 时确定嵌入字体的存储位置。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Embedded font.docx");

// 当我们将带有嵌入字体的文档导出为 .html 时，
// Aspose.Words 可以将字体放置在两种可能的位置。
// 将 "ExportEmbeddedFonts" 标志设置为 "true" 将在 CSS 样式表中存储嵌入字体的原始数据，
// 在 "@font-face" 规则的 "url" 属性中。这可能会创建一个巨大的 CSS 样式表文件
// 并减少此 HTML 转换将创建的外部文件数量。
// 将此标志设置为 "false" 将为每种字体创建一个文件。
// CSS 样式表将使用 "@font-face" 规则的 "url" 属性链接到每个字体文件。
auto htmlFixedSaveOptions = System::MakeObject<Aspose::Words::Saving::HtmlFixedSaveOptions>();
htmlFixedSaveOptions->set_ExportEmbeddedFonts(exportEmbeddedFonts);

doc->Save(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedFonts.html", htmlFixedSaveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedFonts/styles.css");

if (exportEmbeddedFonts)
{
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, u"@font-face { font-family:'Arial'; font-style:normal; font-weight:normal; src:local[(]'☺'[)], url[(].+[)] format[(]'woff'[)]; }")->get_Success());
    ASSERT_EQ(0, System::IO::Directory::GetFiles(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedFonts")->LINQ_Count(static_cast<System::Func<System::String, bool>>(static_cast<std::function<bool(System::String f)>>([](System::String f) -> bool
    {
        return f.EndsWith(u".woff");
    }))));
}
else
{
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, u"@font-face { font-family:'Arial'; font-style:normal; font-weight:normal; src:local[(]'☺'[)], url[(]'font001[.]woff'[)] format[(]'woff'[)]; }")->get_Success());
    ASSERT_EQ(2, System::IO::Directory::GetFiles(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedFonts")->LINQ_Count(static_cast<System::Func<System::String, bool>>(static_cast<std::function<bool(System::String f)>>([](System::String f) -> bool
    {
        return f.EndsWith(u".woff");
    }))));
}
```

## 另见

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
