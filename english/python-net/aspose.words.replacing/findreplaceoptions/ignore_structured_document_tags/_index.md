---
title: ignore_structured_document_tags property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets or sets a boolean value indicating either to ignore content of [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/)"
type: docs
weight: 110
url: /python-net/aspose.words.replacing/findreplaceoptions/ignore_structured_document_tags/
---

## FindReplaceOptions.ignore_structured_document_tags property

Gets or sets a boolean value indicating either to ignore content of [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/).
The default value is ``False``.


When this option is set to ``True``, the content of [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/)
will be treated as a simple text.


Otherwise, [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/) will be processed as standalone Story
and replacing pattern will be searched separately for each [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/),
so that if pattern crosses a [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/), then replacement will not
be performed for such pattern.





### Examples

Shows how to ignore content of tags from replacement.

```python
doc = aw.Document(MY_DIR + "Structured document tags.docx")

# This paragraph contains SDT.
p = doc.first_section.body.get_child(aw.NodeType.PARAGRAPH, 2, True).as_paragraph()
import aspose.words.saving as aws
text_to_search = p.to_string(aw.SaveFormat.TEXT).strip()

options = aw.replacing.FindReplaceOptions()
options.ignore_structured_document_tags = True
doc.range.replace(text_to_search, "replacement", options)

doc.save(ARTIFACTS_DIR + "StructuredDocumentTag.IgnoreStructuredDocumentTags.docx");
```

### See Also

* module [aspose.words.replacing](../../)
* class [FindReplaceOptions](../)

