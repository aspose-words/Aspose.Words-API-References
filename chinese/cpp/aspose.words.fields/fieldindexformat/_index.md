---
title: "Aspose::Words::Fields::FieldIndexFormat 枚举"
linktitle: "FieldIndexFormat"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldIndexFormat 枚举。指定文档中 FieldIndex 字段的格式（使用 C++）。"
type: docs
weight: 129000
url: /zh/cpp/aspose.words.fields/fieldindexformat/
---
## FieldIndexFormat enum


指定文档中 [FieldIndex](../fieldindex/) 字段的格式。

```cpp
enum class FieldIndexFormat
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| Template | 0 | 来自模板。 |
| 经典 | 1 | 经典。 |
| 精致 | 2 | 精致。 |
| Modern | 3 | 现代。 |
| 项目符号 | 4 | 项目符号。 |
| 正式 | 5 | 正式。 |
| 简约 | 6 | 简约。 |


## 示例



展示如何格式化 [FieldIndex](../fieldindex/) 字段。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u"A");
builder->InsertBreak(Aspose::Words::BreakType::LineBreak);
builder->InsertField(u"XE \"A\"");
builder->Write(u"B");

builder->InsertField(u" INDEX \\e \" · \" \\h \"A\" \\c \"2\" \\z \"1033\"", nullptr);

doc->get_FieldOptions()->set_FieldIndexFormat(Aspose::Words::Fields::FieldIndexFormat::Fancy);
doc->UpdateFields();

doc->Save(get_ArtifactsDir() + u"Field.SetFieldIndexFormat.docx");
```

## 另见

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
