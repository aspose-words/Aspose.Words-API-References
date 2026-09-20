---
title: "Aspose::Words::PageSetup::get_LinesPerPage 方法"
linktitle: "get_LinesPerPage"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::PageSetup::get_LinesPerPage 方法。获取或设置 C++ 中文档网格的每页行数。"
type: docs
weight: 26000
url: /zh/cpp/aspose.words/pagesetup/get_linesperpage/
---
## PageSetup::get_LinesPerPage method


获取或设置文档网格中每页的行数。

```cpp
int32_t Aspose::Words::PageSetup::get_LinesPerPage()
```

## 备注


属性的最小值为 1。最大值取决于页面高度和 Normal 样式的字体大小。最小行距为字体大小的 136%。例如，Letter 纸张在一英寸边距下，每页的最大行数为 39。

默认情况下，属性的值使行距为 Normal 样式字体大小的 1.5 倍。

## 示例



展示如何为每页可能的行数指定限制。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 启用间距，然后使用它来设置本节中每页的行数。
// 足够大的字体大小会将部分行推到下一页，以避免字符重叠。
builder->get_PageSetup()->set_LayoutMode(Aspose::Words::SectionLayoutMode::LineGrid);
builder->get_PageSetup()->set_LinesPerPage(15);

builder->get_ParagraphFormat()->set_SnapToGrid(true);

for (int32_t i = 0; i < 30; i++)
{
    builder->Write(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");
}

doc->Save(get_ArtifactsDir() + u"PageSetup.LinesPerPage.docx");
```

## 另见

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
