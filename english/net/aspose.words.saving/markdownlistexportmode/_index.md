---
title: MarkdownListExportMode Enum
linktitle: MarkdownListExportMode
articleTitle: MarkdownListExportMode
second_title: Aspose.Words for .NET
description: Discover how Aspose.Words' MarkdownListExportMode enum enhances list export to Markdown, ensuring precise formatting and seamless integration for your documents.
type: docs
weight: 6100
url: /net/aspose.words.saving/markdownlistexportmode/
---
## MarkdownListExportMode enumeration

Specifies how lists are exported into Markdown.

```csharp
public enum MarkdownListExportMode
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| MarkdownSyntax | `0` | Export list items compatible with Markdown syntax. |
| PlainText | `1` | Export list items as plain text. |

## Examples

Shows how to list items will be written to the markdown document.

```csharp
Document doc = new Document(MyDir + "List item.docx");

// Use MarkdownListExportMode.PlainText or MarkdownListExportMode.MarkdownSyntax to export list.
MarkdownSaveOptions options = new MarkdownSaveOptions { ListExportMode = markdownListExportMode };
doc.Save(ArtifactsDir + "MarkdownSaveOptions.ListExportMode.md", options);
```

### See Also

* namespace [Aspose.Words.Saving](../../aspose.words.saving/)
* assembly [Aspose.Words](../../)
