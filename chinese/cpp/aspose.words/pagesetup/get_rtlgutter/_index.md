---
title: "Aspose::Words::PageSetup::get_RtlGutter 方法"
linktitle: "get_RtlGutter"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::PageSetup::get_RtlGutter 方法。获取或设置 Microsoft Word 是否根据从右到左语言或从左到右语言为该节使用装订线，在 C++ 中。"
type: docs
weight: 40000
url: /zh/cpp/aspose.words/pagesetup/get_rtlgutter/
---
## PageSetup::get_RtlGutter method


获取或设置 Microsoft Word 是否根据从右到左语言或从左到右语言为章节使用装订线。

```cpp
bool Aspose::Words::PageSetup::get_RtlGutter()
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

## 另见

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
