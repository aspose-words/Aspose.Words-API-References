---
title: "Aspose::Words::PageSetup::get_Bidi 方法"
linktitle: "get_Bidi"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::PageSetup::get_Bidi 方法。指定此章节在 C++ 中包含双向（复杂脚本）文本。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words/pagesetup/get_bidi/
---
## PageSetup::get_Bidi method


指定此节包含双向（复杂脚本）文本。

```cpp
bool Aspose::Words::PageSetup::get_Bidi()
```

## 备注


当 **true** 时，此章节中的列从右到左布局。

## 示例



展示如何在章节中设置文本列的顺序。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->get_TextColumns()->SetCount(3);

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u"Column 1.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Write(u"Column 2.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Write(u"Column 3.");

// 将 "Bidi" 属性设置为 "true"，以使列从页面的右侧开始排列。
// 列的顺序将匹配从右到左文本的方向。
// 将 "Bidi" 属性设置为 "false"，以使列从页面的左侧开始排列。
// 列的顺序将匹配从左到右文本的方向。
pageSetup->set_Bidi(reverseColumns);

doc->Save(get_ArtifactsDir() + u"PageSetup.Bidi.docx");
```

## 另见

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
