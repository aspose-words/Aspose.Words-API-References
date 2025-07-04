---
title: Aspose::Words::Saving::MarkdownListExportMode enum
linktitle: MarkdownListExportMode
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::MarkdownListExportMode enum. Specifies how lists are exported into Markdown in C++.'
type: docs
weight: 68000
url: /cpp/aspose.words.saving/markdownlistexportmode/
---
## MarkdownListExportMode enum


Specifies how lists are exported into Markdown.

```cpp
enum class MarkdownListExportMode
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| MarkdownSyntax | 0 | Export list items compatible with Markdown syntax. |
| PlainText | 1 | Export list items as plain text. |


## Examples



Shows how to list items will be written to the markdown document. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List item.docx");

// Use MarkdownListExportMode.PlainText or MarkdownListExportMode.MarkdownSyntax to export list.
auto options = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
options->set_ListExportMode(markdownListExportMode);
doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.ListExportMode.md", options);
```

## See Also

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
