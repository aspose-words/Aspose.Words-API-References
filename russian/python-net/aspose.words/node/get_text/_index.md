---
title: Node.get_text method
linktitle: get_text method
articleTitle: get_text method
second_title: Aspose.Words for Python
description: "Node.get_text method. Gets the text of this node and of all its children."
type: docs
weight: 450
url: /ru/python-net/aspose.words/node/get_text/
---

## get_text() {#default}

Gets the text of this node and of all its children.


```python
def get_text(self):
    ...
```

### Remarks

The returned string includes all control and special characters as described in [ControlChar](../../controlchar/).




### Examples

Shows how to use control characters.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Вставляйте абзацы с текстом с помощью DocumentBuilder.
builder.writeln('Hello world!')
builder.writeln('Hello again!')
# Преобразование документа в текстовый вид показывает, что управляющие символы
# представляют некоторые структурные элементы документа, такие как разрывы страниц.
self.assertEqual(f'Hello world!{aw.ControlChar.CR}' + f'Hello again!{aw.ControlChar.CR}' + aw.ControlChar.PAGE_BREAK, doc.get_text())
# При преобразовании документа в строковый вид,
# мы можем опустить некоторые управляющие символы с помощью метода Trim.
self.assertEqual(f'Hello world!{aw.ControlChar.CR}' + 'Hello again!', doc.get_text().strip())
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
* class [Node](../)

