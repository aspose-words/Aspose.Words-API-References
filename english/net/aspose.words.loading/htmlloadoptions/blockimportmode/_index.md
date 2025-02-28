---
title: HtmlLoadOptions.BlockImportMode
linktitle: BlockImportMode
articleTitle: BlockImportMode
second_title: Aspose.Words for .NET
description: Discover HtmlLoadOptions' BlockImportMode property to customize block-level element imports. Control merging for optimal content management!
type: docs
weight: 20
url: /net/aspose.words.loading/htmlloadoptions/blockimportmode/
---
## HtmlLoadOptions.BlockImportMode property

Gets or sets a value that specifies how properties of block-level elements are imported. Default value is Merge.

```csharp
public BlockImportMode BlockImportMode { get; set; }
```

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

* enum [BlockImportMode](../../blockimportmode/)
* class [HtmlLoadOptions](../)
* namespace [Aspose.Words.Loading](../../../aspose.words.loading/)
* assembly [Aspose.Words](../../../)
