---
title: "Aspose::Words::Saving::MarkdownSaveOptions::get_OfficeMathExportMode 方法"
linktitle: "get_OfficeMathExportMode"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::MarkdownSaveOptions::get_OfficeMathExportMode 方法。指定 OfficeMath 将如何写入输出文件。默认值在 C++ 中为 Text。"
type: docs
weight: 6500
url: /zh/cpp/aspose.words.saving/markdownsaveoptions/get_officemathexportmode/
---
## MarkdownSaveOptions::get_OfficeMathExportMode method


指定 OfficeMath 将如何写入输出文件。默认值为 [Text](../../markdownofficemathexportmode/)。

```cpp
Aspose::Words::Saving::MarkdownOfficeMathExportMode Aspose::Words::Saving::MarkdownSaveOptions::get_OfficeMathExportMode() const
```


## 示例



展示 OfficeMath 将如何写入文档。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
saveOptions->set_OfficeMathExportMode(Aspose::Words::Saving::MarkdownOfficeMathExportMode::Image);

doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.OfficeMathExportMode.md", saveOptions);
```


展示如何将 OfficeMath 对象导出为 Latex。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
saveOptions->set_OfficeMathExportMode(Aspose::Words::Saving::MarkdownOfficeMathExportMode::Latex);

doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.ExportOfficeMathAsLatex.md", saveOptions);
```


展示如何将 OfficeMath 对象导出为 MarkItDown。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
saveOptions->set_OfficeMathExportMode(Aspose::Words::Saving::MarkdownOfficeMathExportMode::MarkItDown);

doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.ExportOfficeMathAsMarkItDown.md", saveOptions);
```

## 另见

* Enum [MarkdownOfficeMathExportMode](../../markdownofficemathexportmode/)
* Class [MarkdownSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
