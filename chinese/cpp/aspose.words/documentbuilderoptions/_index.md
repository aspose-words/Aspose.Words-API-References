---
title: "Aspose::Words::DocumentBuilderOptions 类"
linktitle: "DocumentBuilderOptions"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::DocumentBuilderOptions 类。允许在 C++ 中为文档构建过程指定额外选项。"
type: docs
weight: 22500
url: /zh/cpp/aspose.words/documentbuilderoptions/
---
## DocumentBuilderOptions class


允许为文档构建过程指定附加选项。

```cpp
class DocumentBuilderOptions : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [DocumentBuilderOptions](./documentbuilderoptions/)() |  |
| [get_ContextTableFormatting](./get_contexttableformatting/)() const | 如果应用于表格内容的格式不会影响其后内容的格式，则为 true。默认值为 **true**。 |
| [get_DesignMode](./get_designmode/)() const | 对应于 Microsoft Word 中的设计模式。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_ContextTableFormatting](./set_contexttableformatting/)(bool) | 用于设置 [Aspose::Words::DocumentBuilderOptions::get_ContextTableFormatting](./get_contexttableformatting/)。 |
| [set_DesignMode](./set_designmode/)(bool) | 对应于 Microsoft Word 中的设计模式。 |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
