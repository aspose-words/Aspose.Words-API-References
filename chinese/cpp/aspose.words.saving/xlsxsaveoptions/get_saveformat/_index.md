---
title: "Aspose::Words::Saving::XlsxSaveOptions::get_SaveFormat 方法"
linktitle: "get_SaveFormat"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::XlsxSaveOptions::get_SaveFormat 方法。指定在使用此保存选项对象时文档将保存的格式。只能是 Xlsx（在 C++ 中）。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words.saving/xlsxsaveoptions/get_saveformat/
---
## XlsxSaveOptions::get_SaveFormat method


指定在使用此保存选项对象时文档将保存的格式。只能是 [Xlsx](../../../aspose.words/saveformat/)。

```cpp
Aspose::Words::SaveFormat Aspose::Words::Saving::XlsxSaveOptions::get_SaveFormat() override
```


## 示例



展示如何压缩 XLSX 文档。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shape with linked chart.docx");

auto xlsxSaveOptions = System::MakeObject<Aspose::Words::Saving::XlsxSaveOptions>();
xlsxSaveOptions->set_CompressionLevel(Aspose::Words::Saving::CompressionLevel::Maximum);
xlsxSaveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Xlsx);

doc->Save(get_ArtifactsDir() + u"XlsxSaveOptions.CompressXlsx.xlsx", xlsxSaveOptions);
```

## 另见

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [XlsxSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
