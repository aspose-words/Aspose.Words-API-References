---
title: FindReplaceOptions.IgnoreStructuredDocumentTags
linktitle: IgnoreStructuredDocumentTags
articleTitle: IgnoreStructuredDocumentTags
second_title: Aspose.Words for .NET
description: Discover the FindReplaceOptions IgnoreStructuredDocumentTags property. Control if StructuredDocumentTag content is ignored with this easy-to-use boolean setting.
type: docs
weight: 130
url: /net/aspose.words.replacing/findreplaceoptions/ignorestructureddocumenttags/
---
## FindReplaceOptions.IgnoreStructuredDocumentTags property

Gets or sets a boolean value indicating either to ignore content of [`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/). The default value is `false`.

```csharp
public bool IgnoreStructuredDocumentTags { get; set; }
```

## Remarks

When this option is set to `true`, the content of [`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) will be treated as a simple text.

Otherwise, [`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) will be processed as standalone Story and replacing pattern will be searched separately for each [`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/), so that if pattern crosses a [`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/), then replacement will not be performed for such pattern.

## Examples

Shows how to ignore content of tags from replacement.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");

// This paragraph contains SDT.
Paragraph p = (Paragraph)doc.FirstSection.Body.GetChild(NodeType.Paragraph, 2, true);
string textToSearch = p.ToString(SaveFormat.Text).Trim();

FindReplaceOptions options = new FindReplaceOptions() { IgnoreStructuredDocumentTags = true };
doc.Range.Replace(textToSearch, "replacement", options);

doc.Save(ArtifactsDir + "StructuredDocumentTag.IgnoreStructuredDocumentTags.docx");
```

### See Also

* class [FindReplaceOptions](../)
* namespace [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* assembly [Aspose.Words](../../../)
