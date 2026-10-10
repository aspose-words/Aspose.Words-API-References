---
title: "Aspose::Words::Saving::MarkdownListExportMode 枚举"
linktitle: "MarkdownListExportMode"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::MarkdownListExportMode 枚举。指定在 C++ 中列表如何导出为 Markdown。"
type: docs
weight: 68000
url: /zh/cpp/aspose.words.saving/markdownlistexportmode/
---
## MarkdownListExportMode enum


指定列表如何导出为 Markdown。

```cpp
enum class MarkdownListExportMode
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| MarkdownSyntax | 0 | 导出兼容 Markdown 语法的列表项。 |
| 纯文本 | 1 | 将列表项导出为纯文本。 |


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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
