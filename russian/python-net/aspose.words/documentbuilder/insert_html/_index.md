---
title: DocumentBuilder.insert_html method
linktitle: insert_html method
articleTitle: insert_html method
second_title: Aspose.Words for Python
description: "aspose.words.DocumentBuilder.insert_html method"
type: docs
weight: 380
url: /ru/python-net/aspose.words/documentbuilder/insert_html/
---

## insert_html(html) {#str}

Inserts an HTML string into the document.


```python
def insert_html(self, html: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| html | str | An HTML string to insert into the document. |

### Remarks

You can use this method to insert an HTML fragment or whole HTML document.


## insert_html(html, use_builder_formatting) {#str_bool}

Inserts an HTML string into the document.


```python
def insert_html(self, html: str, use_builder_formatting: bool):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| html | str | An HTML string to insert into the document. |
| use_builder_formatting | bool | A value indicating whether formatting specified in [DocumentBuilder](../) is used as base formatting for text imported from HTML. |

### Remarks

You can use this method to insert an HTML fragment or whole HTML document.

When *useBuilderFormatting* is``False``,
[DocumentBuilder](../) formatting is ignored and formatting of inserted text
is based on default HTML formatting. As a result, the text looks as it is rendered in browsers.


When *useBuilderFormatting* is``True``,
formatting of inserted text is based on [DocumentBuilder](../) formatting,
and the text looks as if it were inserted with [DocumentBuilder.write()](../write/#str).





## insert_html(html, options) {#str_htmlinsertoptions}

Inserts an HTML string into the document. Allows to specify additional options.


```python
def insert_html(self, html: str, options: aspose.words.HtmlInsertOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| html | str | An HTML string to insert into the document. |
| options | [HtmlInsertOptions](../../htmlinsertoptions/) | Options that are used when HTML string is inserted. |

### Remarks

You can use this method to insert an HTML fragment or whole HTML document.


## Examples

Shows how to use a document builder to insert html content into a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
html = "<p align='right'>Paragraph right</p>" + '<b>Implicit paragraph left</b>' + "<div align='center'>Div center</div>" + "<h1 align='left'>Heading 1 left.</h1>"
builder.insert_html(html=html)
# Вставка HTML‑кода разбирает форматирование каждого элемента в эквивалентное форматирование текста документа.
paragraphs = doc.first_section.body.paragraphs
self.assertEqual('Paragraph right', paragraphs[0].get_text().strip())
self.assertEqual(aw.ParagraphAlignment.RIGHT, paragraphs[0].paragraph_format.alignment)
self.assertEqual('Implicit paragraph left', paragraphs[1].get_text().strip())
self.assertEqual(aw.ParagraphAlignment.LEFT, paragraphs[1].paragraph_format.alignment)
self.assertTrue(paragraphs[1].runs[0].font.bold)
self.assertEqual('Div center', paragraphs[2].get_text().strip())
self.assertEqual(aw.ParagraphAlignment.CENTER, paragraphs[2].paragraph_format.alignment)
self.assertEqual('Heading 1 left.', paragraphs[3].get_text().strip())
self.assertEqual('Heading 1', paragraphs[3].paragraph_format.style.name)
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.InsertHtml.docx')
```

Shows how to apply a document builder's formatting while inserting HTML content.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
# Установите выравнивание текста для построителя, вставьте HTML‑абзац с указанным выравниванием и один без него.
builder.paragraph_format.alignment = aw.ParagraphAlignment.DISTRIBUTED
builder.insert_html("<p align='right'>Paragraph 1.</p>" + '<p>Paragraph 2.</p>', use_builder_formatting)
paragraphs = doc.first_section.body.paragraphs
# В первом абзаце указано выравнивание. Когда \"insert_html\" разбирает HTML‑код,
# значение выравнивания абзаца, найденное в HTML‑коде, всегда переходит над значением построителя документа.
self.assertEqual('Paragraph 1.', paragraphs[0].get_text().strip())
self.assertEqual(aw.ParagraphAlignment.RIGHT, paragraphs[0].paragraph_format.alignment)
# Во втором абзаце выравнивание не указано. Его значение выравнивания может быть заполнено
# значением построителя в зависимости от флага, который мы передали методу \"insert_html\".
self.assertEqual('Paragraph 2.', paragraphs[1].get_text().strip())
self.assertEqual(aw.ParagraphAlignment.DISTRIBUTED if use_builder_formatting else aw.ParagraphAlignment.LEFT, paragraphs[1].paragraph_format.alignment)
doc.save(ARTIFACTS_DIR + 'DocumentBuilder.insert_html_with_formatting.docx')
```

## See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

