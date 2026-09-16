---
title: "Aspose::Words::TextColumnCollection::SetCount 方法"
linktitle: "SetCount"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::TextColumnCollection::SetCount 方法。在 C++ 中将文本排列为指定数量的文本列。"
type: docs
weight: 13000
url: /zh/cpp/aspose.words/textcolumncollection/setcount/
---
## TextColumnCollection::SetCount method


将文本排列为指定数量的文本列。

```cpp
void Aspose::Words::TextColumnCollection::SetCount(int32_t newCount)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| newCount | int32_t | 文本要排列成的列数。 |
## 备注


当 [EvenlySpaced](../get_evenlyspaced/) 为 **false** 且您增加列数时，会创建宽度和间距为零的新 [TextColumn](../../textcolumn/) 对象。您需要为新列设置宽度和间距。

## 示例



展示如何在节中创建多个均匀间隔的列。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::TextColumnCollection> columns = builder->get_PageSetup()->get_TextColumns();
columns->set_Spacing(100);
columns->SetCount(2);

builder->Writeln(u"Column 1.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Writeln(u"Column 2.");

doc->Save(get_ArtifactsDir() + u"PageSetup.ColumnsSameWidth.docx");
```

## 另见

* Class [TextColumnCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
