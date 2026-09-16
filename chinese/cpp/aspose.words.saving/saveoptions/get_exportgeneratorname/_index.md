---
title: "Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName 方法"
linktitle: "get_ExportGeneratorName"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName 方法。设置为 true 时，会将 Aspose.Words 的名称和版本嵌入生成的文件中。此属性在 C++ 中的默认值为 true。"
type: docs
weight: 9000
url: /zh/cpp/aspose.words.saving/saveoptions/get_exportgeneratorname/
---
## SaveOptions::get_ExportGeneratorName method


当 **true** 时，会将 Aspose.Words 的名称和版本嵌入生成的文件中。默认值为 **true**。

```cpp
bool Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName() const
```


## 示例



展示如何禁用将 Aspose.Words 的名称和版本添加到生成的文件中。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// 使用 https://docs.aspose.com/words/net/generator-or-producer-name-included-in-output-documents/ 了解如何检查结果。
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_ExportGeneratorName(false);

doc->Save(get_ArtifactsDir() + u"OoxmlSaveOptions.ExportGeneratorName.docx", saveOptions);
```

## 另见

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
