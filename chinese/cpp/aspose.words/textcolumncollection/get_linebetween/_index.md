---
title: "Aspose::Words::TextColumnCollection::get_LineBetween 方法"
linktitle: "get_LineBetween"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::TextColumnCollection::get_LineBetween 方法。当为 true 时，在 C++ 中在列之间添加垂直线。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words/textcolumncollection/get_linebetween/
---
## TextColumnCollection::get_LineBetween method


当 **true** 时，在列之间添加一条垂直线。

```cpp
bool Aspose::Words::TextColumnCollection::get_LineBetween()
```


## 示例



展示如何使用垂直线分隔列。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 配置当前节的 PageSetup 对象，将文本划分为多列。
// 将 "LineBetween" 属性设置为 "true"，以在列之间放置分隔线。
// 将 "LineBetween" 属性设置为 "false"，以使列之间的空间保持为空白。
System::SharedPtr<Aspose::Words::TextColumnCollection> columns = builder->get_PageSetup()->get_TextColumns();
columns->set_LineBetween(lineBetween);
columns->SetCount(3);

builder->Writeln(u"Column 1.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Writeln(u"Column 2.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Writeln(u"Column 3.");

doc->Save(get_ArtifactsDir() + u"PageSetup.VerticalLineBetweenColumns.docx");
```

## 另见

* Class [TextColumnCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
