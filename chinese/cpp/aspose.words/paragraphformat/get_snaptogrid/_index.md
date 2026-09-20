---
title: "Aspose::Words::ParagraphFormat::get_SnapToGrid 方法"
linktitle: "get_SnapToGrid"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::ParagraphFormat::get_SnapToGrid 方法。指定当前段落在 C++ 中布局段落内容时，是否应使用文档每页的网格线设置。"
type: docs
weight: 30000
url: /zh/cpp/aspose.words/paragraphformat/get_snaptogrid/
---
## ParagraphFormat::get_SnapToGrid method


指定当前段落在布局内容时是否应使用文档每页网格线设置。

```cpp
bool Aspose::Words::ParagraphFormat::get_SnapToGrid()
```


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

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
