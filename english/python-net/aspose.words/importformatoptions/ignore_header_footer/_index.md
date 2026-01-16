---
title: ImportFormatOptions.ignore_header_footer property
linktitle: ignore_header_footer property
articleTitle: ignore_header_footer property
second_title: Aspose.Words for Python
description: "ImportFormatOptions.ignore_header_footer property. Gets or sets a boolean value that specifies that source formatting of headers/footers content ignored if [ImportFormatMode.KEEP_SOURCE_FORMATTING](../../importformatmode/#KEEP_SOURCE_FORMATTING) mode is used"
type: docs
weight: 50
url: /python-net/aspose.words/importformatoptions/ignore_header_footer/
---

## ImportFormatOptions.ignore_header_footer property

Gets or sets a boolean value that specifies that source formatting of headers/footers content ignored
if [ImportFormatMode.KEEP_SOURCE_FORMATTING](../../importformatmode/#KEEP_SOURCE_FORMATTING) mode is used.
The default value is ``True``.



```python
@property
def ignore_header_footer(self) -> bool:
    ...

@ignore_header_footer.setter
def ignore_header_footer(self, value: bool):
    ...

```

### Examples

Shows how to specifies ignoring or not source formatting of headers/footers content.

```python
dst_doc = aw.Document(file_name=MY_DIR + 'Document.docx')
src_doc = aw.Document(file_name=MY_DIR + 'Header and footer types.docx')
# If 'IgnoreHeaderFooter' is false then the original formatting for header/footer content
# from "Header and footer types.docx" will be used.
# If 'IgnoreHeaderFooter' is true then the formatting for header/footer content
# from "Document.docx" will be used.
import_format_options = aw.ImportFormatOptions()
import_format_options.ignore_header_footer = False
dst_doc.append_document(src_doc=src_doc, import_format_mode=aw.ImportFormatMode.KEEP_SOURCE_FORMATTING, import_format_options=import_format_options)
dst_doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.DoNotIgnoreHeaderFooter.docx')
```

### See Also

* module [aspose.words](../../)
* class [ImportFormatOptions](../)

