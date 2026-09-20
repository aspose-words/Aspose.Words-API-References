---
title: "Aspose::Words::DocumentBuilderOptions::get_ContextTableFormatting 方法"
linktitle: "get_ContextTableFormatting"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::DocumentBuilderOptions::get_ContextTableFormatting 方法。若应用于表格内容的格式化不影响其后内容的格式化，则为 true。默认值在 C++ 中为 true。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words/documentbuilderoptions/get_contexttableformatting/
---
## DocumentBuilderOptions::get_ContextTableFormatting method


如果应用于表格内容的格式不会影响其后内容的格式，则为 true。默认值为 **true**。

```cpp
bool Aspose::Words::DocumentBuilderOptions::get_ContextTableFormatting() const
```


## 示例



展示如何忽略后续内容的表格格式。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builderOptions = System::MakeObject<Aspose::Words::DocumentBuilderOptions>();
builderOptions->set_ContextTableFormatting(true);
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc, builderOptions);

// 在表格之前添加内容。
// 默认字体大小为 12。
builder->Writeln(u"Font size 12 here.");
builder->StartTable();
builder->InsertCell();
// 更改表格内部的字体大小。
builder->get_Font()->set_Size(5);
builder->Write(u"Font size 5 here");
builder->InsertCell();
builder->Write(u"Font size 5 here");
builder->EndRow();
builder->EndTable();

// 如果 ContextTableFormatting 为 true，则表格格式不会应用于后续内容。
// 如果 ContextTableFormatting 为 false，则表格格式将在之后的内容上应用。
builder->Writeln(u"Font size 12 here.");

doc->Save(get_ArtifactsDir() + u"Table.ContextTableFormatting.docx");
```

## 另见

* Class [DocumentBuilderOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
