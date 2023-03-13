---
title: force_copy_styles property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets or sets a boolean value indicating either to copy conflicting styles in [ImportFormatMode.KEEP_SOURCE_FORMATTING](../../importformatmode/#KEEP_SOURCE_FORMATTING) mode"
type: docs
weight: 30
url: /python-net/aspose.words/importformatoptions/force_copy_styles/
---

## ImportFormatOptions.force_copy_styles property

Gets or sets a boolean value indicating either to copy conflicting styles
in [ImportFormatMode.KEEP_SOURCE_FORMATTING](../../importformatmode/#KEEP_SOURCE_FORMATTING) mode.
The default value is ``False``.


By default, if a matching style already exists in a destination document, the source style formatting
is expanded into direct node attributes and the style of this node is reset to a default.

When this option is set to ``True``, the source style will be forcibly copied
into destination document with unique name and applied to the imported node.

Note, in this case it is not guaranteed that formatting of the imported node in destination document
will be preserved.




### Examples

Shows how to copy source styles with unique names forcibly.

```python
# Both documents contain MyStyle1 and MyStyle2, MyStyle3 exists only in a source document.
src_doc = aw.Document(MY_DIR + "Styles source.docx");
dst_doc = aw.Document(MY_DIR + "Styles destination.docx");

options = aw.ImportFormatOptions()
options.force_copy_styles = True
dst_doc.append_document(src_doc, aw.ImportFormatMode.KEEP_SOURCE_FORMATTING, options)

paras = dst_doc.sections[1].body.paragraphs

self.assertEqual(paras[0].paragraph_format.style.name, "MyStyle1_0")
self.assertEqual(paras[1].paragraph_format.style.name, "MyStyle2_0")
self.assertEqual(paras[2].paragraph_format.style.name, "MyStyle3")
```

### See Also

* module [aspose.words](../../)
* class [ImportFormatOptions](../)

