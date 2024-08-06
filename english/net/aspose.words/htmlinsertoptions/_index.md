---
title: HtmlInsertOptions Enum
linktitle: HtmlInsertOptions
articleTitle: HtmlInsertOptions
second_title: Aspose.Words for .NET
description: Aspose.Words.HtmlInsertOptions enum. Specifies options for the InsertHtml method in C#.
type: docs
weight: 3400
url: /net/aspose.words/htmlinsertoptions/
---
## HtmlInsertOptions enumeration

Specifies options for the [`InsertHtml`](../documentbuilder/inserthtml/) method.

```csharp
[Flags]
public enum HtmlInsertOptions
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| None | `0` | Use the default options when inserting HTML. |
| UseBuilderFormatting | `1` | Use font and paragraph formatting specified in [`DocumentBuilder`](../documentbuilder/) as base formatting for text inserted from HTML. |
| RemoveLastEmptyParagraph | `2` | Remove the empty paragraph that is normally inserted after HTML that ends with a block-level element. |
| PreserveBlocks | `4` | Preserve properties of block-level elements. |

## Examples

Shows how to allows better preserve borders and margins seen.

```csharp
const string html = @"
    <html>
        <div style='border:dotted'>
        <div style='border:solid'>
            <p>paragraph 1</p>
            <p>paragraph 2</p>
        </div>
        </div>
    </html>";

// Set the new mode of import HTML block-level elements.
HtmlInsertOptions insertOptions = HtmlInsertOptions.PreserveBlocks;

DocumentBuilder builder = new DocumentBuilder();
builder.InsertHtml(html, insertOptions);
builder.Document.Save(ArtifactsDir + "DocumentBuilder.PreserveBlocks.docx");
```

### See Also

* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
