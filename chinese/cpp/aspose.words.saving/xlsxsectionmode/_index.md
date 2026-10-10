---
title: "Aspose::Words::Saving::XlsxSectionMode 枚举"
linktitle: "XxlsxSectionMode"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::XlsxSectionMode 枚举。指定在 C++ 中将文档保存为 XLSX 格式时如何处理章节。"
type: docs
weight: 87000
url: /zh/cpp/aspose.words.saving/xlsxsectionmode/
---
## XlsxSectionMode enum


指定在将文档保存为 XLSX 格式时如何处理节。

```cpp
enum class XlsxSectionMode
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| MultipleWorksheets | 0 | 指定为文档的每个章节创建一个单独的工作表。 |
| SingleWorksheet | 1 | 指定文档的所有章节保存到同一个工作表上。 |


## 示例



展示如何将文档保存为单独的工作表。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");

// 文档的每个章节将被创建为单独的工作表。
// 使用 'SingleWorksheet' 在单个工作表上显示整个文档。
auto xlsxSaveOptions = System::MakeObject<Aspose::Words::Saving::XlsxSaveOptions>();
xlsxSaveOptions->set_SectionMode(Aspose::Words::Saving::XlsxSectionMode::MultipleWorksheets);

doc->Save(get_ArtifactsDir() + u"XlsxSaveOptions.SelectionMode.xlsx", xlsxSaveOptions);
```

## 另见

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
