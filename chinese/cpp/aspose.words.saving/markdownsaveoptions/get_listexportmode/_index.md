---
title: "Aspose::Words::Saving::MarkdownSaveOptions::get_ListExportMode 方法"
linktitle: "get_ListExportMode"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::MarkdownSaveOptions::get_ListExportMode 方法。指定列表项将如何写入输出文件。默认值在 C++ 中为 MarkdownSyntax。"
type: docs
weight: 6000
url: /zh/cpp/aspose.words.saving/markdownsaveoptions/get_listexportmode/
---
## MarkdownSaveOptions::get_ListExportMode method


指定列表项将如何写入输出文件。默认值是 [MarkdownSyntax](../../markdownlistexportmode/)。

```cpp
Aspose::Words::Saving::MarkdownListExportMode Aspose::Words::Saving::MarkdownSaveOptions::get_ListExportMode() const
```

## 备注


当此属性设置为 [PlainText](../../markdownlistexportmode/) 时，所有列表标签将使用 [UpdateListLabels](../../../aspose.words/document/updatelistlabels/) 更新，并以其实际值导出。在这种情况下，此类列表可能与 Markdown 格式不兼容，导入时将被识别为纯文本。

当此属性设置为 [MarkdownSyntax](../../markdownlistexportmode/) 时，写入器尝试以允许 Markdown 自动编号列表项的方式导出列表项。

## 示例



显示列表项将如何写入 Markdown 文档。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List item.docx");

// 使用 MarkdownListExportMode.PlainText 或 MarkdownListExportMode.MarkdownSyntax 导出列表。
auto options = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
options->set_ListExportMode(markdownListExportMode);
doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.ListExportMode.md", options);
```

## 另见

* Enum [MarkdownListExportMode](../../markdownlistexportmode/)
* Class [MarkdownSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
