---
title: ExportHeadersFootersMode enumeration
linktitle: ExportHeadersFootersMode enumeration
articleTitle: ExportHeadersFootersMode enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.ExportHeadersFootersMode enumeration. Specifies how headers and footers are exported to HTML, MHTML or EPUB."
type: docs
weight: 180
url: /zh/python-net/aspose.words.saving/exportheadersfootersmode/
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
# 此文档包含页眉和页脚。我们可以通过 "HeadersFooters" 集合访问它们。
self.assertEqual('First header', doc.first_section.headers_footers.get_by_header_footer_type(aw.HeaderFooterType.HEADER_FIRST).get_text().strip())
# 像 .html 这样的格式不会将文档拆分为页面，因此页眉/页脚的功能将不同。
# 当我们使用 Microsoft Word 将文档打开为 .docx 时，它们会正常工作。
# 如果我们将包含页眉/页脚的文档转换为 html，转换过程会将页眉/页脚合并到正文中。
# 我们可以使用 SaveOptions 对象在转换为 html 时省略页眉/页脚。
save_options = aw.saving.HtmlSaveOptions(aw.SaveFormat.HTML)
save_options.export_headers_footers_mode = aw.saving.ExportHeadersFootersMode.NONE
doc.save(file_name=ARTIFACTS_DIR + 'HeaderFooter.ExportMode.html', save_options=save_options)
# 打开已保存的文档并验证其中不包含页眉的文本。
doc = aw.Document(file_name=ARTIFACTS_DIR + 'HeaderFooter.ExportMode.html')
self.assertFalse('First header' in doc.range.text)
```

### See Also

* module [aspose.words.saving](../)
* property [HtmlSaveOptions.export_headers_footers_mode](../htmlsaveoptions/export_headers_footers_mode/)

