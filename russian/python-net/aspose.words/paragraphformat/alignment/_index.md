---
title: ParagraphFormat.alignment property
linktitle: alignment property
articleTitle: alignment property
second_title: Aspose.Words for Python
description: "ParagraphFormat.alignment property. Gets or sets text alignment for the paragraph."
type: docs
weight: 30
url: /ru/python-net/aspose.words/paragraphformat/alignment/
---

## ParagraphFormat.alignment property

Gets or sets text alignment for the paragraph.


```python
@property
def alignment(self) -> aspose.words.ParagraphAlignment:
    ...

@alignment.setter
def alignment(self, value: aspose.words.ParagraphAlignment):
    ...

```

### Examples

Shows how to insert a paragraph into the document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
font = builder.font
font.size = 16
font.bold = True
font.color = aspose.pydrawing.Color.blue
font.name = 'Arial'
font.underline = aw.Underline.DASH
paragraph_format = builder.paragraph_format
paragraph_format.first_line_indent = 8
paragraph_format.alignment = aw.ParagraphAlignment.JUSTIFY
paragraph_format.add_space_between_far_east_and_alpha = True
paragraph_format.add_space_between_far_east_and_digit = True
paragraph_format.keep_together = True
# Метод "Writeln" завершает абзац после добавления текста
# а затем начинается новая строка, добавляя новый абзац.
builder.writeln('Hello world!')
self.assertTrue(builder.current_paragraph.is_end_of_document)
```

Shows how to construct an Aspose.Words document by hand.

```python
doc = aw.Document()
# Пустой документ содержит один раздел, одно тело и один абзац.
# Вызовите метод "RemoveAllChildren", чтобы удалить все эти узлы,
# и получите узел документа без дочерних элементов.
doc.remove_all_children()
# В этом документе теперь нет составных дочерних узлов, к которым можно добавить содержимое.
# Если мы хотим его отредактировать, нам потребуется заново заполнить его коллекцию узлов.
# Сначала создайте новый раздел, а затем добавьте его как дочерний к корневому узлу документа.
section = aw.Section(doc)
doc.append_child(section)
# Установите некоторые свойства настройки страницы для раздела.
section.page_setup.section_start = aw.SectionStart.NEW_PAGE
section.page_setup.paper_size = aw.PaperSize.LETTER
# Разделу требуется тело, которое будет содержать и отображать всё его содержимое
# на странице между заголовком и нижним колонтитулом раздела.
body = aw.Body(doc)
section.append_child(body)
# Создайте абзац, задайте некоторые свойства форматирования и затем добавьте его как дочерний к телу.
para = aw.Paragraph(doc)
para.paragraph_format.style_name = 'Heading 1'
para.paragraph_format.alignment = aw.ParagraphAlignment.CENTER
body.append_child(para)
# Наконец, добавьте некоторое содержимое в документ. Создайте пробег,
# задать его внешний вид и содержимое, а затем добавить его как дочерний к абзацу.
run = aw.Run(doc=doc)
run.text = 'Hello World!'
run.font.color = aspose.pydrawing.Color.red
para.append_child(run)
self.assertEqual('Hello World!', doc.get_text().strip())
doc.save(file_name=ARTIFACTS_DIR + 'Section.CreateManually.docx')
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

