---
title: DocumentBuilder constructor
linktitle: DocumentBuilder constructor
articleTitle: DocumentBuilder constructor
second_title: Aspose.Words for Python
description: "aspose.words.DocumentBuilder constructor"
type: docs
weight: 10
url: /ru/python-net/aspose.words/documentbuilder/__init__/
---

## DocumentBuilder() {#default}

Initializes a new instance of this class.


```python
def __init__(self):
    ...
```

### Remarks

Creates a new [DocumentBuilder](../) object and attaches it to a new [Document](../../document/) object.



## DocumentBuilder(options) {#documentbuilderoptions}

Initializes a new instance of this class.


```python
def __init__(self, options: aspose.words.DocumentBuilderOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| options | [DocumentBuilderOptions](../../documentbuilderoptions/) |  |

### Remarks

Creates a new [DocumentBuilder](../) object and attaches it to a new [Document](../../document/) object.
Additional document building options can be specified.



## DocumentBuilder(doc) {#document}

Initializes a new instance of this class.


```python
def __init__(self, doc: aspose.words.Document):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| doc | [Document](../../document/) | The [Document](../../document/) object to attach to. |

### Remarks

Creates a new [DocumentBuilder](../) object, attaches to the specified [Document](../../document/) object.
The cursor is positioned at the beginning of the document.



## DocumentBuilder(doc, options) {#document_documentbuilderoptions}

Initializes a new instance of this class.


```python
def __init__(self, doc: aspose.words.Document, options: aspose.words.DocumentBuilderOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| doc | [Document](../../document/) | The [Document](../../document/) object to attach to. |
| options | [DocumentBuilderOptions](../../documentbuilderoptions/) | Additional options for the document building process. |

### Remarks

Creates a new [DocumentBuilder](../) object, attaches to the specified [Document](../../document/) object.
The cursor is positioned at the beginning of the document.



## Examples

Shows how to ignore table formatting for content after.

```python
doc = aw.Document()
builder_options = aw.DocumentBuilderOptions()
builder_options.context_table_formatting = True
builder = aw.DocumentBuilder(doc=doc, options=builder_options)
# Добавляет содержимое перед таблицей.
# Размер шрифта по умолчанию — 12.
builder.writeln('Font size 12 here.')
builder.start_table()
builder.insert_cell()
# Изменяет размер шрифта внутри таблицы.
builder.font.size = 5
builder.write('Font size 5 here')
builder.insert_cell()
builder.write('Font size 5 here')
builder.end_row()
builder.end_table()
# Если ContextTableFormatting равно true, то форматирование таблицы не применяется к последующему содержимому.
# Если ContextTableFormatting равно false, то форматирование таблицы применяется к последующему содержимому.
builder.writeln('Font size 12 here.')
doc.save(file_name=ARTIFACTS_DIR + 'Table.ContextTableFormatting.docx')
```

Shows how to create headers and footers in a document using DocumentBuilder.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Укажите, что нам нужны разные колонтитулы для первой, чётных и нечётных страниц.
builder.page_setup.different_first_page_header_footer = True
builder.page_setup.odd_and_even_pages_header_footer = True
# Создайте колонтитулы, затем добавьте в документ три страницы, чтобы отобразить каждый тип колонтитула.
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_FIRST)
builder.write('Header for the first page')
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_EVEN)
builder.write('Header for even pages')
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_PRIMARY)
builder.write('Header for all other pages')
builder.move_to_section(0)
builder.writeln('Page1')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Page2')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Page3')
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.HeadersAndFooters.docx')
```

Shows how to insert a Table of contents (TOC) into a document using heading styles as entries.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Вставьте оглавление на первую страницу документа.
# Настройте таблицу так, чтобы она захватывала абзацы с заголовками уровней от 1 до 3.
# Также установите, чтобы её элементы были гиперссылками, которые перенаправят нас
# к месту заголовка при щелчке левой кнопкой мыши в Microsoft Word.
builder.insert_table_of_contents('\\o "1-3" \\h \\z \\u')
builder.insert_break(aw.BreakType.PAGE_BREAK)
# Заполните оглавление, добавив абзацы со стилями заголовков.
# Каждый такой заголовок уровня от 1 до 3 создаст запись в таблице.
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1
builder.writeln('Heading 1')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING2
builder.writeln('Heading 1.1')
builder.writeln('Heading 1.2')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1
builder.writeln('Heading 2')
builder.writeln('Heading 3')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING2
builder.writeln('Heading 3.1')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING3
builder.writeln('Heading 3.1.1')
builder.writeln('Heading 3.1.2')
builder.writeln('Heading 3.1.3')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING4
builder.writeln('Heading 3.1.3.1')
builder.writeln('Heading 3.1.3.2')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING2
builder.writeln('Heading 3.2')
builder.writeln('Heading 3.3')
# Оглавление — это поле определённого типа, которое необходимо обновить, чтобы отобразить актуальный результат.
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.InsertToc.docx')
```

## See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

