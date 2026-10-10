---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_FontResourcesSubsettingSizeThreshold 方法"
linktitle: "get_FontResourcesSubsettingSizeThreshold"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_FontResourcesSubsettingSizeThreshold 方法。控制在保存为 HTML、MHTML 或 EPUB 时哪些字体资源需要子集化。默认值在 C++ 中为 %0。"
type: docs
weight: 31000
url: /zh/cpp/aspose.words.saving/htmlsaveoptions/get_fontresourcessubsettingsizethreshold/
---
## HtmlSaveOptions::get_FontResourcesSubsettingSizeThreshold method


控制在保存为 HTML、MHTML 或 EPUB 时哪些字体资源需要子集化。默认值为 **%0**。

```cpp
int32_t Aspose::Words::Saving::HtmlSaveOptions::get_FontResourcesSubsettingSizeThreshold() const
```

## 备注


[ExportFontResources](../get_exportfontresources/) allows exporting fonts as subsidiary files or as parts of the output package. If the document uses many fonts, especially with large number of glyphs, then output size can grow significantly. [Font](../../../aspose.words/font/) subsetting reduces the size of the exported font resource by filtering out glyphs that are not used by the current document.

[Font](../../../aspose.words/font/) subsetting works as follows:

* By default, all exported fonts are subsetted.
* Setting [FontResourcesSubsettingSizeThreshold](./) to a positive value instructs Aspose.Words to subset fonts which file size is larger than the specified value.
* Setting the property to **MaxValue** suppresses font subsetting.



**Important!** When exporting font resources, font licensing issues should be considered. Authors who want to use specific fonts via a downloadable font mechanism must always carefully verify that their intended use is within the scope of the font license. Many commercial fonts presently do not allow web downloading of their fonts in any form. [License](../../../aspose.words/license/) agreements that cover some fonts specifically note that usage via **%@font-face** rules in CSS style sheets is not allowed. [Font](../../../aspose.words/font/) subsetting can also violate license terms.

## 示例



展示如何使用字体子集化。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Arial");
builder->Writeln(u"Hello world!");
builder->get_Font()->set_Name(u"Times New Roman");
builder->Writeln(u"Hello world!");
builder->get_Font()->set_Name(u"Courier New");
builder->Writeln(u"Hello world!");

// 当我们将文档保存为 HTML 时，我们可以传递一个 SaveOptions 对象来配置字体子集化。
// 假设我们将 "ExportFontResources" 标志设置为 "true"，并在 "FontsFolder" 属性中指定一个文件夹。
// 在这种情况下，保存操作将创建该文件夹并在其中放置一个 .ttf 文件。
// 该文件夹中为文档使用的每种字体放置一个文件。
// 每个 .ttf 文件将包含该字体的完整字形集，
// 这可能导致随文档一起的文件非常大。
// 当我们对字体进行子集化时，导出的原始数据只会包含文档中使用的字形
// 而不是完整的字形集。如果文档中的文本仅使用了该字体的一小部分
// 字形集，那么子集化将显著减小输出文档的大小。
// 我们可以使用 "FontResourcesSubsettingSizeThreshold" 属性来定义 .ttf 文件的大小（字节）。
// 如果导出的字体文件大小超过该阈值，保存操作将对该字体进行子集化。
// 将阈值设为 0 将对所有字体应用子集化，
// 而将其设置为 "int.MaxValue" 则实际上禁用子集化。
System::String fontsFolder = get_ArtifactsDir() + u"HtmlSaveOptions.FontSubsetting.Fonts";

auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportFontResources(true);
options->set_FontsFolder(fontsFolder);
options->set_FontResourcesSubsettingSizeThreshold(fontResourcesSubsettingSizeThreshold);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.FontSubsetting.html", options);

System::ArrayPtr<System::String> fontFileNames = System::IO::Directory::GetFiles(fontsFolder)->LINQ_Where(static_cast<System::Func<System::String, bool>>(static_cast<std::function<bool(System::String s)>>([](System::String s) -> bool
{
    return s.EndsWith(u".ttf");
})))->LINQ_ToArray();

ASSERT_EQ(3, fontFileNames->get_Length());

for (System::String filename : fontFileNames)
{
    // 默认情况下，我们的三种字体对应的 .ttf 文件大小都将超过 700MB。
    // 子集化后它们全部将降至 30MB 以下。
    auto fontFileInfo = System::MakeObject<System::IO::FileInfo>(filename);

    ASSERT_TRUE(fontFileInfo->get_Length() > 700000 || fontFileInfo->get_Length() < 30000);
    ASSERT_TRUE(System::Math::Max(fontResourcesSubsettingSizeThreshold, 30000) > System::MakeObject<System::IO::FileInfo>(filename)->get_Length());
}
```

## 另见

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
