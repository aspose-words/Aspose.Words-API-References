---
title: "Aspose::Words::Saving::MarkdownExportAsHtml 枚举"
linktitle: "MarkdownExportAsHtml"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::MarkdownExportAsHtml 枚举。允许在 C++ 中指定要以原始 HTML 导出到 Markdown 的元素。"
type: docs
weight: 66500
url: /zh/cpp/aspose.words.saving/markdownexportashtml/
---
## MarkdownExportAsHtml enum


允许指定要以原始 HTML 导出到 Markdown 的元素。

```cpp
enum class MarkdownExportAsHtml
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| None | 0 | 使用 Markdown 语法导出所有元素，不包含任何原始 HTML。 |
| 表格 | 1 | 将表格导出为原始 HTML。 |
| NonCompatibleTables | 2 | 将无法在纯 Markdown 中正确表示的表格导出为原始 HTML。 |


## 示例



展示如何将表格导出为 Markdown 的原始 HTML。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Sample table:");

// 创建表格。
builder->InsertCell();
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Right);
builder->Write(u"Cell1");
builder->InsertCell();
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
builder->Write(u"Cell2");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
saveOptions->set_ExportAsHtml(Aspose::Words::Saving::MarkdownExportAsHtml::Tables);

doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.ExportTableAsHtml.md", saveOptions);
```

## 另见

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
