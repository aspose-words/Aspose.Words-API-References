---
title: ExportHeadersFootersMode enumeration
linktitle: ExportHeadersFootersMode enumeration
articleTitle: ExportHeadersFootersMode enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.ExportHeadersFootersMode enumeration. Specifies how headers and footers are exported to HTML, MHTML or EPUB."
type: docs
weight: 180
url: /ar/python-net/aspose.words.saving/exportheadersfootersmode/
---

## ExportHeadersFootersMode enumeration

Specifies how headers and footers are exported to HTML, MHTML or EPUB.


### Members

| Name | Description |
| --- | --- |
| NONE | Headers and footers are not exported. |
| PER_SECTION | Primary headers and footers are exported at the beginning and the end of each section. |
| FIRST_SECTION_HEADER_LAST_SECTION_FOOTER | Primary header of the first section is exported at the beginning of the document and primary footer is at the end. |
| FIRST_PAGE_HEADER_FOOTER_PER_SECTION | First page header and footer are exported at the beginning and the end of each section. |

### Examples

Shows how to omit headers/footers when saving a document to HTML.

```python
doc = aw.Document(file_name=MY_DIR + 'Header and footer types.docx')
# يحتوي هذا المستند على رؤوس وتذييلات. يمكننا الوصول إليها عبر مجموعة "HeadersFooters".
self.assertEqual('First header', doc.first_section.headers_footers.get_by_header_footer_type(aw.HeaderFooterType.HEADER_FIRST).get_text().strip())
# الصيغ مثل .html لا تقسم المستند إلى صفحات، لذا لن تعمل الرؤوس/التذييلات بنفس الطريقة.
# كما يحدث عندما نفتح المستند كملف .docx باستخدام Microsoft Word.
# إذا قمنا بتحويل مستند يحتوي على رؤوس/تذييلات إلى html، فإن التحويل سيدمج الرؤوس/التذييلات في نص الجسم.
# يمكننا استخدام كائن SaveOptions لتجاهل الرؤوس/التذييلات أثناء التحويل إلى html.
save_options = aw.saving.HtmlSaveOptions(aw.SaveFormat.HTML)
save_options.export_headers_footers_mode = aw.saving.ExportHeadersFootersMode.NONE
doc.save(file_name=ARTIFACTS_DIR + 'HeaderFooter.ExportMode.html', save_options=save_options)
# افتح المستند المحفوظ وتأكد من أنه لا يحتوي على نص الرأس.
doc = aw.Document(file_name=ARTIFACTS_DIR + 'HeaderFooter.ExportMode.html')
self.assertFalse('First header' in doc.range.text)
```

### See Also

* module [aspose.words.saving](../)
* property [HtmlSaveOptions.export_headers_footers_mode](../htmlsaveoptions/export_headers_footers_mode/)

