---
title: "Aspose::Words::PageVerticalAlignment enum"
linktitle: "PageVerticalAlignment"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::PageVerticalAlignment enum. 指定 C++ 中每页文本的垂直对齐方式。"
type: docs
weight: 108000
url: /zh/cpp/aspose.words/pageverticalalignment/
---
## PageVerticalAlignment enum


指定每页文本的垂直对齐方式。

```cpp
enum class PageVerticalAlignment
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| 底部 | 3 | 文本在页面底部对齐。 |
| 居中 | 1 | 文本在页面中部对齐。 |
| 两端对齐 | 2 | 文本展开以填满页面。 |
| 顶部 | 0 | 文本在页面顶部对齐。 |


## 示例



展示如何对文档中的节应用和恢复页面设置。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 修改构建器当前节的页面设置属性并添加文本。
builder->get_PageSetup()->set_Orientation(Aspose::Words::Orientation::Landscape);
builder->get_PageSetup()->set_VerticalAlignment(Aspose::Words::PageVerticalAlignment::Center);
builder->Writeln(u"This is the first section, which landscape oriented with vertically centered text.");

// 如果我们使用文档构建器开始新节，
// 它将继承构建器当前的页面设置属性。
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);

ASSERT_EQ(Aspose::Words::Orientation::Landscape, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_Orientation());
ASSERT_EQ(Aspose::Words::PageVerticalAlignment::Center, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_VerticalAlignment());

// 我们可以使用 "ClearFormatting" 方法将其页面设置属性恢复为默认值。
builder->get_PageSetup()->ClearFormatting();

ASSERT_EQ(Aspose::Words::Orientation::Portrait, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_Orientation());
ASSERT_EQ(Aspose::Words::PageVerticalAlignment::Top, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_VerticalAlignment());

builder->Writeln(u"This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

doc->Save(get_ArtifactsDir() + u"PageSetup.ClearFormatting.docx");
```

## 另见

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
