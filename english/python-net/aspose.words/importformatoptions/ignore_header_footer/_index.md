---
title: ignore_header_footer property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets or sets a boolean value that specifies that source formatting of headers/footers content ignored if [ImportFormatMode.KEEP_SOURCE_FORMATTING](../../importformatmode/#KEEP_SOURCE_FORMATTING) mode is used"
type: docs
weight: 30
url: /python-net/aspose.words/importformatoptions/ignore_header_footer/
---

## ImportFormatOptions.ignore_header_footer property

Gets or sets a boolean value that specifies that source formatting of headers/footers content ignored
if [ImportFormatMode.KEEP_SOURCE_FORMATTING](../../importformatmode/#KEEP_SOURCE_FORMATTING) mode is used.
The default value is ``true``.



### Examples

Shows how to specifies ignoring or not source formatting of headers/footers content.

```python
dst_doc = aw.Document(MY_DIR + "Document.docx")
src_doc = aw.Document(MY_DIR + "Header and footer types.docx")

import_format_options = aw.ImportFormatOptions()
import_format_options.ignore_header_footer = False

dst_doc.append_document(src_doc, aw.ImportFormatMode.KEEP_SOURCE_FORMATTING, import_format_options)

dst_doc.save(ARTIFACTS_DIR + "DocumentBuilder.do_not_ignore_header_footer.docx")
```

### See Also

* module [aspose.words](../../)
* class [ImportFormatOptions](../)

