---
title: "Aspose::Words::Saving::XlsxSaveOptions::get_SectionMode 方法"
linktitle: "get_SectionMode"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::XlsxSaveOptions::get_SectionMode 方法。获取或设置在保存输出 XLSX 文档时如何处理章节。默认值在 C++ 中为 MultipleWorksheets。"
type: docs
weight: 4500
url: /zh/cpp/aspose.words.saving/xlsxsaveoptions/get_sectionmode/
---
## XlsxSaveOptions::get_SectionMode method


获取或设置在保存输出 XLSX 文档时如何处理章节。默认值为 [MultipleWorksheets](../../xlsxsectionmode/)。

```cpp
Aspose::Words::Saving::XlsxSectionMode Aspose::Words::Saving::XlsxSaveOptions::get_SectionMode() const
```


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

* Enum [XlsxSectionMode](../../xlsxsectionmode/)
* Class [XlsxSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
