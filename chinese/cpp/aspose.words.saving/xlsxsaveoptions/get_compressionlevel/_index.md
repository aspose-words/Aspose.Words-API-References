---
title: "Aspose::Words::Saving::XlsxSaveOptions::get_CompressionLevel 方法"
linktitle: "get_CompressionLevel"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::XlsxSaveOptions::get_CompressionLevel 方法。指定用于保存文档的压缩级别。默认值在 C++ 中为 Normal。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words.saving/xlsxsaveoptions/get_compressionlevel/
---
## XlsxSaveOptions::get_CompressionLevel method


指定用于保存文档的压缩级别。默认值为 [Normal](../../compressionlevel/)。

```cpp
Aspose::Words::Saving::CompressionLevel Aspose::Words::Saving::XlsxSaveOptions::get_CompressionLevel() const
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

* Enum [CompressionLevel](../../compressionlevel/)
* Class [XlsxSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
