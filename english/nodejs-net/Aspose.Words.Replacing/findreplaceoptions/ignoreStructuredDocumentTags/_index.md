---
title: FindReplaceOptions.ignoreStructuredDocumentTags property
linktitle: ignoreStructuredDocumentTags property
articleTitle: ignoreStructuredDocumentTags property
second_title: Aspose.Words for NodeJs
description: "FindReplaceOptions.ignoreStructuredDocumentTags property. Gets or sets a boolean value indicating either to ignore content of [StructuredDocumentTag](../../../Aspose.Words.Markup/structureddocumenttag/)"
type: docs
weight: 120
url: /nodejs-net/Aspose.Words.Replacing/findreplaceoptions/ignoreStructuredDocumentTags/
---

## FindReplaceOptions.ignoreStructuredDocumentTags property

Gets or sets a boolean value indicating either to ignore content of [StructuredDocumentTag](../../../Aspose.Words.Markup/structureddocumenttag/).
The default value is ``False``.



```js
get ignoreStructuredDocumentTags(): boolean
```

### Remarks

When this option is set to ``True``, the content of [StructuredDocumentTag](../../../Aspose.Words.Markup/structureddocumenttag/)
will be treated as a simple text.


Otherwise, [StructuredDocumentTag](../../../Aspose.Words.Markup/structureddocumenttag/) will be processed as standalone Story
and replacing pattern will be searched separately for each [StructuredDocumentTag](../../../Aspose.Words.Markup/structureddocumenttag/),
so that if pattern crosses a [StructuredDocumentTag](../../../Aspose.Words.Markup/structureddocumenttag/), then replacement will not
be performed for such pattern.





### Examples

Shows how to ignore content of tags from replacement.

```js
let doc = new aw.Document(base.myDir + "Structured document tags.docx");

// This paragraph contains SDT.
let p = doc.firstSection.body.getChild(aw.NodeType.Paragraph, 2, true).asParagraph();
let textToSearch = p.toString(aw.SaveFormat.Text).trim();

let options = new aw.Replacing.FindReplaceOptions();
options.ignoreStructuredDocumentTags = true;
doc.range.replace(textToSearch, "replacement", options);

doc.save(base.artifactsDir + "StructuredDocumentTag.ignoreStructuredDocumentTags.docx");
```

### See Also

* module [Aspose.Words.Replacing](../../)
* class [FindReplaceOptions](../)

