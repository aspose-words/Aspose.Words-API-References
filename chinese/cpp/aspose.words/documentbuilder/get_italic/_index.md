---
title: "Aspose::Words::DocumentBuilder::get_Italic method"
linktitle: "get_Italic"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::DocumentBuilder::get_Italic 方法。如果字体在 C++ 中被设置为斜体，则返回 True。"
type: docs
weight: 21000
url: /zh/cpp/aspose.words/documentbuilder/get_italic/
---
## DocumentBuilder::get_Italic method


如果字体设置为斜体，则为 True。

```cpp
bool Aspose::Words::DocumentBuilder::get_Italic()
```


## 示例



展示如何使用 DocumentBuilder 填充 MERGEFIELD，而不是使用邮件合并。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 插入一些 MERGEFIELD，这些字段在邮件合并期间接受来自数据源中同名列的数据，
// 然后手动填充它们。
builder->InsertField(u" MERGEFIELD Chairman ");
builder->InsertField(u" MERGEFIELD ChiefFinancialOfficer ");
builder->InsertField(u" MERGEFIELD ChiefTechnologyOfficer ");

builder->MoveToMergeField(u"Chairman");
builder->set_Bold(true);
builder->Writeln(u"John Doe");

builder->MoveToMergeField(u"ChiefFinancialOfficer");
builder->set_Italic(true);
builder->Writeln(u"Jane Doe");

builder->MoveToMergeField(u"ChiefTechnologyOfficer");
builder->set_Italic(true);
builder->Writeln(u"John Bloggs");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.FillMergeFields.docx");
```

## 另见

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
