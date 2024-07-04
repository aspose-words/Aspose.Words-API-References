---
title: MarkdownSaveOptions.ListExportMode
linktitle: ListExportMode
articleTitle: ListExportMode
second_title: Aspose.Words for .NET
description: MarkdownSaveOptions ListExportMode property. Specifies how list items will be written to the output file. Default value is MarkdownSyntax in C#.
type: docs
weight: 80
url: /net/aspose.words.saving/markdownsaveoptions/listexportmode/
---
## MarkdownSaveOptions.ListExportMode property

Specifies how list items will be written to the output file. Default value is MarkdownSyntax.

```csharp
public MarkdownListExportMode ListExportMode { get; set; }
```

## Remarks

When this property is set to PlainText all list labels are updated using [`UpdateListLabels`](../../../aspose.words/document/updatelistlabels/) and exported with their actual values. Such lists can be non-compatible with Markdown format and will be recognized as plain text upon importing in this case.

When this property is set to MarkdownSyntax, writer tries to export list items in manner that allows to numerate list items in automatic mode by Markdown.

## Examples

Shows how to list items will be written to the markdown document.

```csharp
Document doc = new Document(MyDir + "List item.docx");

// Use MarkdownListExportMode.PlainText or MarkdownListExportMode.MarkdownSyntax to export list.
MarkdownSaveOptions options = new MarkdownSaveOptions { ListExportMode = markdownListExportMode };
doc.Save(ArtifactsDir + "MarkdownSaveOptions.ListExportMode.md", options);
```

### See Also

* enum [MarkdownListExportMode](../../markdownlistexportmode/)
* class [MarkdownSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
