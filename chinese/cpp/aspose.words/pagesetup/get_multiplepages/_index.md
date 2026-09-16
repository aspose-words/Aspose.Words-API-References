---
title: "Aspose::Words::PageSetup::get_MultiplePages 方法"
linktitle: "get_MultiplePages"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::PageSetup::get_MultiplePages 方法。对于多页文档，获取或设置文档的打印或渲染方式，以便在 C++ 中可以装订成小册子。"
type: docs
weight: 29000
url: /zh/cpp/aspose.words/pagesetup/get_multiplepages/
---
## PageSetup::get_MultiplePages method


对于多页文档，获取或设置文档的打印或渲染方式，以便可以装订成小册子。

```cpp
Aspose::Words::Settings::MultiplePagesType Aspose::Words::PageSetup::get_MultiplePages() const
```


## 示例



展示如何设置装订线边距。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// 插入跨越多页的文本。
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
for (int32_t i = 0; i < 6; i++)
{
    builder->Write(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
}

// 装订线会在左侧或右侧页边距添加空白，
// 这弥补了书本页面中心折叠对页面布局的侵占。
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();

// 确定页面在页边距内可用于文本的空间量，然后添加一定量来填充页边距。
ASSERT_NEAR(470.30, pageSetup->get_PageWidth() - pageSetup->get_LeftMargin() - pageSetup->get_RightMargin(), 0.01);

pageSetup->set_Gutter(100.0);

// 将 "RtlGutter" 属性设置为 "true"，以在从右到左的文本中将装订线放置在更合适的位置。
pageSetup->set_RtlGutter(true);

// 将 "MultiplePages" 属性设置为 "MultiplePagesType.MirrorMargins" 以交替
// 每页左右两侧的页边距位置。
pageSetup->set_MultiplePages(Aspose::Words::Settings::MultiplePagesType::MirrorMargins);

doc->Save(get_ArtifactsDir() + u"PageSetup.Gutter.docx");
```


展示如何配置可以打印为书折的文档。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// 插入跨越 16 页的文本。
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"My Booklet:");

for (int32_t i = 0; i < 15; i++)
{
    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
    builder->Write(System::String::Format(u"Booklet face #{0}", i));
}

// 配置第一节的 \"PageSetup\" 属性，以书折形式打印文档。
// 当我们双面打印此文档时，可以将页面取出堆叠它们
// 并一次性沿中线全部折叠。文档的内容将对齐成书折。
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->set_MultiplePages(Aspose::Words::Settings::MultiplePagesType::BookFoldPrinting);

// 我们只能以 4 的倍数指定纸张数量。
pageSetup->set_SheetsPerBooklet(4);

doc->Save(get_ArtifactsDir() + u"PageSetup.Booklet.docx");
```

## 另见

* Enum [MultiplePagesType](../../../aspose.words.settings/multiplepagestype/)
* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
