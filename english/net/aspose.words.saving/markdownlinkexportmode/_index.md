---
title: MarkdownLinkExportMode Enum
linktitle: MarkdownLinkExportMode
articleTitle: MarkdownLinkExportMode
second_title: Aspose.Words for .NET
description: Aspose.Words.Saving.MarkdownLinkExportMode enum. Specifies how links are exported into Markdown in C#.
type: docs
weight: 5610
url: /net/aspose.words.saving/markdownlinkexportmode/
---
## MarkdownLinkExportMode enumeration

Specifies how links are exported into Markdown.

```csharp
public enum MarkdownLinkExportMode
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Auto | `0` | Automatically detect export mode for each link. |
| Inline | `1` | Export all links as inline blocks. |
| Reference | `2` | Export all links as reference blocks. |

## Examples

Shows how to links will be written to the .md file.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertShape(ShapeType.Balloon, 100, 100);

// Image will be written as reference:
// ![ref1]
//
// [ref1]: aw_ref.001.png
MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
saveOptions.LinkExportMode = MarkdownLinkExportMode.Reference;
doc.Save(ArtifactsDir + "MarkdownSaveOptions.LinkExportMode.Reference.md", saveOptions);

// Image will be written as inline:
// ![](aw_inline.001.png)
saveOptions.LinkExportMode = MarkdownLinkExportMode.Inline;
doc.Save(ArtifactsDir + "MarkdownSaveOptions.LinkExportMode.Inline.md", saveOptions);
```

### See Also

* namespace [Aspose.Words.Saving](../../aspose.words.saving/)
* assembly [Aspose.Words](../../)
