---
title: Body constructor
linktitle: Body constructor
articleTitle: Body constructor
second_title: Aspose.Words for Python
description: "Body constructor. Initializes a new instance of the [Body](../) class."
type: docs
weight: 10
url: /ru/python-net/aspose.words/body/__init__/
---

## Body(doc) {#documentbase}

Initializes a new instance of the [Body](../) class.



```python
def __init__(self, doc: aspose.words.DocumentBase):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| doc | [DocumentBase](../../documentbase/) | The owner document. |

### Remarks

When [Body](../) is created, it belongs to the specified document, but is not 
yet part of the document and [Node.parent_node](../../node/parent_node/) is ``None``.

To append [Body](../) to a [Section](../../section/) use [CompositeNode.append_child()](../../compositenode/append_child/#node)
[CompositeNode.insert_after()](../../compositenode/insert_after/#node_node) or [CompositeNode.insert_before()](../../compositenode/insert_before/#node_node)
methods.




### Examples

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
* class [Body](../)

