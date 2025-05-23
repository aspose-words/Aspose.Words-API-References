---
title: BlockImportMode Enum
linktitle: BlockImportMode
articleTitle: BlockImportMode
second_title: Aspose.Words for .NET
description: Discover how the Aspose.Words.BlockImportMode enum enhances HTML document integration by optimizing block-level element property imports for seamless workflows.
type: docs
weight: 4010
url: /net/aspose.words.loading/blockimportmode/
---
## BlockImportMode enumeration

Specifies how properties of block-level elements are imported from HTML-based documents.

```csharp
public enum BlockImportMode
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Merge | `0` | Properties of parent blocks are merged and stored on child elements (i.e. paragraphs or tables). |
| Preserve | `1` | Properties of parent blocks are imported to a special logical structure and are stored separately from document nodes. |

## Examples

Shows how properties of block-level elements are imported from HTML-based documents.

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
MemoryStream stream = new MemoryStream(Encoding.UTF8.GetBytes(html));

HtmlLoadOptions loadOptions = new HtmlLoadOptions();
// Set the new mode of import HTML block-level elements.
loadOptions.BlockImportMode = blockImportMode;

Document doc = new Document(stream, loadOptions);
doc.Save(ArtifactsDir + "HtmlLoadOptions.BlockImport.docx");
```

### See Also

* namespace [Aspose.Words.Loading](../../aspose.words.loading/)
* assembly [Aspose.Words](../../)
