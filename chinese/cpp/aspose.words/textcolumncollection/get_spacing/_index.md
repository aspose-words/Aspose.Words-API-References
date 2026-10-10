---
title: "Aspose::Words::TextColumnCollection::get_Spacing 方法"
linktitle: "get_Spacing"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::TextColumnCollection::get_Spacing 方法。 当列均匀间距时，以点为单位获取或设置每列之间的间距（C++）。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words/textcolumncollection/get_spacing/
---
## TextColumnCollection::get_Spacing method


当列均匀间隔时，获取或设置每列之间的间距（单位：点）。

```cpp
double Aspose::Words::TextColumnCollection::get_Spacing()
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

* Class [TextColumnCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
