---
title: "Aspose::Words::Saving::MarkdownOfficeMathExportMode 枚举"
linktitle: "MarkdownOfficeMathExportMode"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::MarkdownOfficeMathExportMode 枚举。指定 Aspose.Words 在 C++ 中如何将 OfficeMath 导出为 Markdown。"
type: docs
weight: 68500
url: /zh/cpp/aspose.words.saving/markdownofficemathexportmode/
---
## MarkdownOfficeMathExportMode enum


指定 Aspose.Words 如何将 OfficeMath 导出为 Markdown。

```cpp
enum class MarkdownOfficeMathExportMode
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| 文本 | 0 | 将 OfficeMath 导出为纯文本。 |
| 图像 | 1 | 将 OfficeMath 导出为图像。 |
| MathML | 2 | 将 OfficeMath 导出为 MathML。 |
| Latex | 3 | 将 OfficeMath 导出为 LaTeX。 |
| MarkItDown | 4 | 将 OfficeMath 导出为兼容 MarkItDown 的 LaTeX。 |


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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
