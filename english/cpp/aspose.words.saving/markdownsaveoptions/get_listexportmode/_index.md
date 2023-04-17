---
title: Aspose::Words::Saving::MarkdownSaveOptions::get_ListExportMode method
linktitle: get_ListExportMode
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::MarkdownSaveOptions::get_ListExportMode method. Specifies how list items will be written to the output file. Default value is MarkdownSyntax in C++.'
type: docs
weight: 6000
url: /cpp/aspose.words.saving/markdownsaveoptions/get_listexportmode/
---
## MarkdownSaveOptions::get_ListExportMode method


Specifies how list items will be written to the output file. Default value is [MarkdownSyntax](../../markdownlistexportmode/).

```cpp
Aspose::Words::Saving::MarkdownListExportMode Aspose::Words::Saving::MarkdownSaveOptions::get_ListExportMode() const
```

## Remarks


When this property is set to [PlainText](../../markdownlistexportmode/) all list labels are updated using [UpdateListLabels](../../../aspose.words/document/updatelistlabels/) and exported with their actual values. Such lists can be non-compatible with Markdown format and will be recognized as plain text upon importing in this case.

When this property is set to [MarkdownSyntax](../../markdownlistexportmode/), writer tries to export list items in manner that allows to numerate list items in automatic mode by Markdown. 
## See Also

* Enum [MarkdownListExportMode](../../markdownlistexportmode/)
* Class [MarkdownSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
