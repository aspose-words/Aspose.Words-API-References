---
title: TxtSaveOptionsBase.export_headers_footers_mode property
linktitle: export_headers_footers_mode property
articleTitle: export_headers_footers_mode property
second_title: Aspose.Words for Python
description: "TxtSaveOptionsBase.export_headers_footers_mode property. Specifies the way headers and footers are exported to the text formats"
type: docs
weight: 20
url: /ru/python-net/aspose.words.saving/txtsaveoptionsbase/export_headers_footers_mode/
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
# Вставьте чётные и основные колонтитулы в документ.
# Основные колонтитулы будут переопределять чётные колонтитулы.
doc.first_section.headers_footers.add(aw.HeaderFooter(doc, aw.HeaderFooterType.HEADER_EVEN))
doc.first_section.headers_footers.get_by_header_footer_type(aw.HeaderFooterType.HEADER_EVEN).append_paragraph('Even header')
doc.first_section.headers_footers.add(aw.HeaderFooter(doc, aw.HeaderFooterType.FOOTER_EVEN))
doc.first_section.headers_footers.get_by_header_footer_type(aw.HeaderFooterType.FOOTER_EVEN).append_paragraph('Even footer')
doc.first_section.headers_footers.add(aw.HeaderFooter(doc, aw.HeaderFooterType.HEADER_PRIMARY))
doc.first_section.headers_footers.get_by_header_footer_type(aw.HeaderFooterType.HEADER_PRIMARY).append_paragraph('Primary header')
doc.first_section.headers_footers.add(aw.HeaderFooter(doc, aw.HeaderFooterType.FOOTER_PRIMARY))
doc.first_section.headers_footers.get_by_header_footer_type(aw.HeaderFooterType.FOOTER_PRIMARY).append_paragraph('Primary footer')
# Вставьте страницы, чтобы отобразить эти колонтитулы.
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Page 1')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Page 2')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.write('Page 3')
# Создайте объект "TxtSaveOptions", который мы можем передать методу "Save" документа
# чтобы изменить способ сохранения документа в простой текст.
save_options = aw.saving.TxtSaveOptions()
# Установите свойство "ExportHeadersFootersMode" в "TxtExportHeadersFootersMode.None"
# чтобы не экспортировать никакие колонтитулы.
# Установите свойство "ExportHeadersFootersMode" в "TxtExportHeadersFootersMode.PrimaryOnly"
# чтобы экспортировать только основные колонтитулы.
# Установите свойство "ExportHeadersFootersMode" в "TxtExportHeadersFootersMode.AllAtEnd"
# чтобы разместить все колонтитулы для всех секций в конце документа.
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

