---
title: ImportFormatOptions.append_document_with_new_page property
linktitle: append_document_with_new_page property
articleTitle: append_document_with_new_page property
second_title: Aspose.Words for Python
description: "ImportFormatOptions.append_document_with_new_page property. Gets or sets a boolean value indicating whether to change a first imported section type to the [SectionStart.NEW_PAGE](../../sectionstart/#NEW_PAGE) forcibly when call [Document.append_document()](../../document/append_document/#document_importformatmode_importformatoptions)"
type: docs
weight: 30
url: /python-net/aspose.words/importformatoptions/append_document_with_new_page/
---

## ImportFormatOptions.append_document_with_new_page property

Gets or sets a boolean value indicating whether to change a first imported section type
to the [SectionStart.NEW_PAGE](../../sectionstart/#NEW_PAGE) forcibly when call
[Document.append_document()](../../document/append_document/#document_importformatmode_importformatoptions).
The default value is ``True``.




```python
@property
def append_document_with_new_page(self) -> bool:
    ...

@append_document_with_new_page.setter
def append_document_with_new_page(self, value: bool):
    ...

```

### Remarks

Please note that this option is only relevant for the
[Document.append_document()](../../document/append_document/#document_importformatmode_importformatoptions)
method and has no effect on other import-related methods.




### Examples

Shows how to preserve original section type.

```python
dst_doc = aw.Document()
src_doc = aw.Document()
src_doc.first_section.page_setup.section_start = aw.SectionStart.CONTINUOUS
options = aw.ImportFormatOptions()
options.append_document_with_new_page = False
dst_doc.append_document(src_doc=src_doc, import_format_mode=aw.ImportFormatMode.KEEP_SOURCE_FORMATTING, import_format_options=options)
self.assertEqual(aw.SectionStart.CONTINUOUS, dst_doc.sections[1].page_setup.section_start)
```

### See Also

* module [aspose.words](../../)
* class [ImportFormatOptions](../)

