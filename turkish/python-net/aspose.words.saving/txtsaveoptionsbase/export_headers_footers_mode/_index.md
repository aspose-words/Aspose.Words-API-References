---
title: TxtSaveOptionsBase.export_headers_footers_mode property
linktitle: export_headers_footers_mode property
articleTitle: export_headers_footers_mode property
second_title: Aspose.Words for Python
description: "TxtSaveOptionsBase.export_headers_footers_mode property. Specifies the way headers and footers are exported to the text formats"
type: docs
weight: 20
url: /tr/python-net/aspose.words.saving/txtsaveoptionsbase/export_headers_footers_mode/
---

## TxtSaveOptionsBase.export_headers_footers_mode property

Specifies the way headers and footers are exported to the text formats.
Default value is [TxtExportHeadersFootersMode.PRIMARY_ONLY](../../txtexportheadersfootersmode/#PRIMARY_ONLY).



```python
@property
def export_headers_footers_mode(self) -> aspose.words.saving.TxtExportHeadersFootersMode:
    ...

@export_headers_footers_mode.setter
def export_headers_footers_mode(self, value: aspose.words.saving.TxtExportHeadersFootersMode):
    ...

```

### Examples

Shows how to specify how to export headers and footers to plain text format.

```python
doc = aw.Document()
# Belgeye çift ve birincil üstbilgi/altbilgi ekleyin.
# Birincil üstbilgi/altbilgiler, çift numaralı üstbilgi/altbilgilerin üzerine yazacaktır.
doc.first_section.headers_footers.add(aw.HeaderFooter(doc, aw.HeaderFooterType.HEADER_EVEN))
doc.first_section.headers_footers.get_by_header_footer_type(aw.HeaderFooterType.HEADER_EVEN).append_paragraph('Even header')
doc.first_section.headers_footers.add(aw.HeaderFooter(doc, aw.HeaderFooterType.FOOTER_EVEN))
doc.first_section.headers_footers.get_by_header_footer_type(aw.HeaderFooterType.FOOTER_EVEN).append_paragraph('Even footer')
doc.first_section.headers_footers.add(aw.HeaderFooter(doc, aw.HeaderFooterType.HEADER_PRIMARY))
doc.first_section.headers_footers.get_by_header_footer_type(aw.HeaderFooterType.HEADER_PRIMARY).append_paragraph('Primary header')
doc.first_section.headers_footers.add(aw.HeaderFooter(doc, aw.HeaderFooterType.FOOTER_PRIMARY))
doc.first_section.headers_footers.get_by_header_footer_type(aw.HeaderFooterType.FOOTER_PRIMARY).append_paragraph('Primary footer')
# Bu üstbilgi ve altbilgileri göstermek için sayfalar ekleyin.
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Page 1')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Page 2')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.write('Page 3')
# "TxtSaveOptions" nesnesi oluşturun, bunu belgenin "Save" metoduna geçirebiliriz
# belgeyi düz metin olarak nasıl kaydedeceğimizi değiştirmek için.
save_options = aw.saving.TxtSaveOptions()
# "ExportHeadersFootersMode" özelliğini "TxtExportHeadersFootersMode.None" olarak ayarlayın
# herhangi bir üstbilgi/altbilgi dışa aktarılmayacak.
# "ExportHeadersFootersMode" özelliğini "TxtExportHeadersFootersMode.PrimaryOnly" olarak ayarlayın
# yalnızca birincil üstbilgi/altbilgileri dışa aktar.
# "ExportHeadersFootersMode" özelliğini "TxtExportHeadersFootersMode.AllAtEnd" olarak ayarlayın
# tüm bölüm gövdeleri için tüm üstbilgi ve altbilgileri belgenin sonuna yerleştirin.
save_options.export_headers_footers_mode = txt_export_headers_footers_mode
doc.save(file_name=ARTIFACTS_DIR + 'TxtSaveOptions.ExportHeadersFooters.txt', save_options=save_options)
doc_text = system_helper.io.File.read_all_text(ARTIFACTS_DIR + 'TxtSaveOptions.ExportHeadersFooters.txt')
new_line = system_helper.environment.Environment.new_line()
switch_condition = txt_export_headers_footers_mode
if switch_condition == aw.saving.TxtExportHeadersFootersMode.ALL_AT_END:
    self.assertEqual(f'Page 1{new_line}' + f'Page 2{new_line}' + f'Page 3{new_line}' + f'Even header{new_line}{new_line}' + f'Primary header{new_line}{new_line}' + f'Even footer{new_line}{new_line}' + f'Primary footer{new_line}{new_line}', doc_text)
elif switch_condition == aw.saving.TxtExportHeadersFootersMode.PRIMARY_ONLY:
    self.assertEqual(f'Primary header{new_line}' + f'Page 1{new_line}' + f'Page 2{new_line}' + f'Page 3{new_line}' + f'Primary footer{new_line}', doc_text)
elif switch_condition == aw.saving.TxtExportHeadersFootersMode.NONE:
    self.assertEqual(f'Page 1{new_line}' + f'Page 2{new_line}' + f'Page 3{new_line}', doc_text)
```

### See Also

* module [aspose.words.saving](../../)
* class [TxtSaveOptionsBase](../)

