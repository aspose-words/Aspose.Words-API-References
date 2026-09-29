---
title: HtmlSaveOptions.export_toc_page_numbers property
linktitle: export_toc_page_numbers property
articleTitle: export_toc_page_numbers property
second_title: Aspose.Words for Python
description: "HtmlSaveOptions.export_toc_page_numbers property. Specifies whether to write page numbers to table of contents when saving HTML, MHTML and EPUB"
type: docs
weight: 270
url: /ru/python-net/aspose.words.saving/htmlsaveoptions/export_toc_page_numbers/
---

## HtmlSaveOptions.export_toc_page_numbers property

Specifies whether to write page numbers to table of contents when saving HTML, MHTML and EPUB.
Default value is ``False``.



```python
@property
def export_toc_page_numbers(self) -> bool:
    ...

@export_toc_page_numbers.setter
def export_toc_page_numbers(self, value: bool):
    ...

```

### Examples

Shows how to display page numbers when saving a document with a table of contents to .html.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Вставьте оглавление, а затем заполните документ абзацами, отформатированными с использованием стиля "Заголовок"
# стиль, который оглавление будет воспринимать как пункты. Каждый пункт будет отображать абзац заголовка слева,
# и номер страницы, содержащей заголовок, справа.
field_toc = builder.insert_field(field_type=aw.fields.FieldType.FIELD_TOC, update_field=True).as_field_toc()
builder.paragraph_format.style = builder.document.styles.get_by_name('Heading 1')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Entry 1')
builder.writeln('Entry 2')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Entry 3')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Entry 4')
field_toc.update_page_numbers()
doc.update_fields()
# HTML‑документы не имеют страниц. Если мы сохраним этот документ в HTML,
# номера страниц, которые отображает наше оглавление, не будут иметь смысла.
# При сохранении документа в HTML мы можем передать объект SaveOptions, чтобы исключить эти номера страниц из оглавления.
# Если установить флаг "ExportTocPageNumbers" в значение "true",
# каждый пункт оглавления будет отображать заголовок, разделитель и номер страницы, сохраняя его внешний вид в Microsoft Word.
# Если установить флаг "ExportTocPageNumbers" в значение "false",
# операция сохранения исключит как разделитель, так и номер страницы, оставив заголовок каждого пункта нетронутым.
options = aw.saving.HtmlSaveOptions()
options.export_toc_page_numbers = export_toc_page_numbers
doc.save(file_name=ARTIFACTS_DIR + 'HtmlSaveOptions.ExportTocPageNumbers.html', save_options=options)
out_doc_contents = system_helper.io.File.read_all_text(ARTIFACTS_DIR + 'HtmlSaveOptions.ExportTocPageNumbers.html')
if export_toc_page_numbers:
    self.assertTrue('<span>Entry 1</span>' + '<span style="width:428.14pt; font-family:\'Lucida Console\'; font-size:10pt; display:inline-block; -aw-font-family:\'Times New Roman\'; ' + '-aw-tabstop-align:right; -aw-tabstop-leader:dots; -aw-tabstop-pos:469.8pt">.......................................................................</span>' + '<span>2</span>' + '</p>' in out_doc_contents)
else:
    self.assertTrue('<p style="margin-top:0pt; margin-bottom:0pt">' + '<span>Entry 2</span>' + '</p>' in out_doc_contents)
```

### See Also

* module [aspose.words.saving](../../)
* class [HtmlSaveOptions](../)

