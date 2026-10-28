---
title: Aspose::Words::Saving::MarkdownSaveOptions::set_ListExportMode method
linktitle: set_ListExportMode
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::MarkdownSaveOptions::set_ListExportMode method. Specifies how list items will be written to the output file. Default value is MarkdownSyntax in C++.'
type: docs
weight: 14000
url: /cpp/aspose.words.saving/markdownsaveoptions/set_listexportmode/
---
## MarkdownSaveOptions::set_ListExportMode method


Specifies how list items will be written to the output file. Default value is [MarkdownSyntax](../../markdownlistexportmode/).

```cpp
void Aspose::Words::Saving::MarkdownSaveOptions::set_ListExportMode(Aspose::Words::Saving::MarkdownListExportMode value)
```

## Remarks


When this property is set to [PlainText](../../markdownlistexportmode/) all list labels are updated using [UpdateListLabels](../../../aspose.words/document/updatelistlabels/) and exported with their actual values. Such lists can be non-compatible with Markdown format and will be recognized as plain text upon importing in this case.

When this property is set to [MarkdownSyntax](../../markdownlistexportmode/), writer tries to export list items in manner that allows to numerate list items in automatic mode by Markdown.
## Examples


Shows how to list items will be written to the markdown document.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"List item.docx"));

// Use MarkdownListExportMode.PlainText or MarkdownListExportMode.MarkdownSyntax to export list.
auto options = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
options->set_ListExportMode(markdownListExportMode);
doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.ListExportMode.md", options);
```
## See Also

* Class [MarkdownSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
