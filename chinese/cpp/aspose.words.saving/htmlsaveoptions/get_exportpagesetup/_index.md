---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportPageSetup 方法"
linktitle: "get_ExportPageSetup"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportPageSetup 方法。指定是否将页面设置导出为 HTML、MHTML 或 EPUB。默认在 C++ 中为 false。"
type: docs
weight: 24000
url: /zh/cpp/aspose.words.saving/htmlsaveoptions/get_exportpagesetup/
---
## HtmlSaveOptions::get_ExportPageSetup method


指定是否将页面设置导出到 HTML、MHTML 或 EPUB。默认值为 **false**。

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportPageSetup() const
```

## 备注


Aspose.Words 文档模型中的每个 [Section](../../../aspose.words/section/) 都通过 [PageSetup](../../../aspose.words/pagesetup/) 类提供页面设置信息。将文档导出为 HTML 格式时，您可能需要保留这些信息以供后续使用。特别是，页面设置对于渲染为分页媒体（打印）或随后转换为本机 Microsoft Word 文件格式（DOCX、DOC、RTF、WML）可能很重要。

在大多数情况下，HTML 旨在在浏览器中查看，浏览器不会进行分页。因此此功能默认是未激活的。

## 示例



展示如何决定在保存为 HTML 时是否保留章节结构/页面设置信息。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Section 1");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Section 2");

System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->set_TopMargin(36.0);
pageSetup->set_BottomMargin(36.0);
pageSetup->set_PaperSize(Aspose::Words::PaperSize::A5);

// 在将文档保存为 HTML 时，我们可以传入一个 SaveOptions 对象
// 决定是保留还是丢弃页面设置。
// 如果我们将 "ExportPageSetup" 标志设置为 "true"，输出的 HTML 文档将包含我们的页面设置配置。
// 如果我们将 "ExportPageSetup" 标志设置为 "false"，保存操作将丢弃我们的页面设置。
// 对于第一个章节，两个章节将呈现相同的外观。
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportPageSetup(exportPageSetup);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ExportPageSetup.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.ExportPageSetup.html");

if (exportPageSetup)
{
    ASSERT_TRUE(outDocContents.Contains(System::String(u"<style type=\"text/css\">") + u"@page Section_1 { size:419.55pt 595.3pt; margin:36pt 70.85pt; -aw-footer-distance:35.4pt; -aw-header-distance:35.4pt }" + u"@page Section_2 { size:612pt 792pt; margin:70.85pt; -aw-footer-distance:35.4pt; -aw-header-distance:35.4pt }" + u"div.Section_1 { page:Section_1 }div.Section_2 { page:Section_2 }" + u"</style>"));

    ASSERT_TRUE(outDocContents.Contains(System::String(u"<div class=\"Section_1\">") + u"<p style=\"margin-top:0pt; margin-bottom:0pt\">" + u"<span>Section 1</span>" + u"</p>" + u"</div>"));
}
else
{
    ASSERT_FALSE(outDocContents.Contains(u"style type=\"text/css\">"));

    ASSERT_TRUE(outDocContents.Contains(System::String(u"<div>") + u"<p style=\"margin-top:0pt; margin-bottom:0pt\">" + u"<span>Section 1</span>" + u"</p>" + u"</div>"));
}
```

## 另见

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
