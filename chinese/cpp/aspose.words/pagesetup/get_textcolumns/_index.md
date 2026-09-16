---
title: "Aspose::Words::PageSetup::get_TextColumns 方法"
linktitle: "get_TextColumns"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::PageSetup::get_TextColumns 方法。返回一个集合，表示 C++ 中的文本列集合。"
type: docs
weight: 44000
url: /zh/cpp/aspose.words/pagesetup/get_textcolumns/
---
## PageSetup::get_TextColumns method


返回表示文本列集合的集合。

```cpp
System::SharedPtr<Aspose::Words::TextColumnCollection> Aspose::Words::PageSetup::get_TextColumns()
```


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

* Class [TextColumnCollection](../../textcolumncollection/)
* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
