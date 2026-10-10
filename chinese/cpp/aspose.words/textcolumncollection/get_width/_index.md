---
title: "Aspose::Words::TextColumnCollection::get_Width 方法"
linktitle: "get_Width"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::TextColumnCollection::get_Width 方法。当列均匀间距时，获取列的宽度（C++）。"
type: docs
weight: 6000
url: /zh/cpp/aspose.words/textcolumncollection/get_width/
---
## TextColumnCollection::get_Width method


当列均匀间隔时，获取列的宽度。

```cpp
double Aspose::Words::TextColumnCollection::get_Width()
```

## 备注


仅当 [EvenlySpaced](../get_evenlyspaced/) 设置为 **true** 时生效。

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
