---
title: CompositeNode.append_child method
linktitle: append_child method
articleTitle: append_child method
second_title: Aspose.Words for Python
description: "CompositeNode.append_child method. Adds the specified node to the end of the list of child nodes for this node."
type: docs
weight: 80
url: /ru/python-net/aspose.words/compositenode/append_child/
---

## append_child(new_child) {#node}

Adds the specified node to the end of the list of child nodes for this node.


```python
def append_child(self, new_child: aspose.words.Node):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| new_child | [Node](../../node/) | The node to add. |

### Remarks

If the *newChild* is already in the tree, it is first removed.

If the node being inserted was created from another document, you should use 
[DocumentBase.import_node()](../../documentbase/import_node/#node_bool_importformatmode) to import the node to the current document. 
The imported node can then be inserted into the current document.




### Returns

The node added.


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
* class [CompositeNode](../)

