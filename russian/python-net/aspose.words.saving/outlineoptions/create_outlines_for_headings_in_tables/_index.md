---
title: OutlineOptions.create_outlines_for_headings_in_tables property
linktitle: create_outlines_for_headings_in_tables property
articleTitle: create_outlines_for_headings_in_tables property
second_title: Aspose.Words for Python
description: "OutlineOptions.create_outlines_for_headings_in_tables property. Specifies whether or not to create outlines for headings (paragraphs formatted with the Heading styles) inside tables."
type: docs
weight: 40
url: /ru/python-net/aspose.words.saving/outlineoptions/create_outlines_for_headings_in_tables/
---

## OutlineOptions.create_outlines_for_headings_in_tables property

Specifies whether or not to create outlines for headings (paragraphs formatted with the Heading styles) inside tables.


```python
@property
def create_outlines_for_headings_in_tables(self) -> bool:
    ...

@create_outlines_for_headings_in_tables.setter
def create_outlines_for_headings_in_tables(self, value: bool):
    ...

```

### Remarks

Default value is ``False``.




### Examples

Shows how to create PDF document outline entries for headings inside tables.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Создайте таблицу из трёх строк. Первая строка,
# текст которой мы отформатируем в стиле заголовка, будет служить заголовком столбца.
builder.start_table()
builder.insert_cell()
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1
builder.write('Customers')
builder.end_row()
builder.insert_cell()
builder.paragraph_format.style_identifier = aw.StyleIdentifier.NORMAL
builder.write('John Doe')
builder.end_row()
builder.insert_cell()
builder.write('Jane Doe')
builder.end_table()
# Создайте объект "PdfSaveOptions", который мы можем передать методу "Save" документа
# чтобы изменить способ, которым этот метод конвертирует документ в .PDF.
pdf_save_options = aw.saving.PdfSaveOptions()
# Выходной PDF‑документ будет содержать оглавление, которое представляет собой таблицу содержания, перечисляющую заголовки в теле документа.
# Щелчок по элементу в этой структуре перенесёт нас к месту соответствующего заголовка.
# Установите свойство "HeadingsOutlineLevels" в значение "1", чтобы получить схему
# чтобы регистрировать только заголовки уровнем не более 1.
pdf_save_options.outline_options.headings_outline_levels = 1
# Установите свойство "CreateOutlinesForHeadingsInTables" в значение "false", чтобы исключить все заголовки внутри таблиц,
# например, созданную выше, из схемы.
# Установите свойство "CreateOutlinesForHeadingsInTables" в значение "true", чтобы включить все заголовки внутри таблиц
# в схему, при условии, что их уровень заголовка не превышает значение свойства "HeadingsOutlineLevels".
pdf_save_options.outline_options.create_outlines_for_headings_in_tables = create_outlines_for_headings_in_tables
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.TableHeadingOutlines.pdf', save_options=pdf_save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [OutlineOptions](../)

