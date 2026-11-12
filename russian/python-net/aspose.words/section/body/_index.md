---
title: Section.body property
linktitle: body property
articleTitle: body property
second_title: Aspose.Words for Python
description: "Section.body property. Returns the [Body](../../body/) child node of the section."
type: docs
weight: 20
url: /ru/python-net/aspose.words/section/body/
---

## Section.body property

Returns the [Body](../../body/) child node of the section.



```python
@property
def body(self) -> aspose.words.Body:
    ...

```

### Remarks

[Body](../../body/) contains main text of the section.

Returns ``None`` if the section does not have a [Body](../../body/) node among its children.




### Examples

Clears main text from all sections from the document leaving the sections themselves.

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
# Разделу требуется тело, которое будет содержать и отображать всё его содержимое
# на странице между заголовком и нижним колонтитулом раздела.
body = aw.Body(doc)
section.append_child(body)
# Это тело не имеет дочерних элементов, поэтому пока нельзя добавить в него элементы run.
self.assertEqual(0, doc.first_section.body.get_child_nodes(aw.NodeType.ANY, True).count)
# Вызовите "EnsureMinimum", чтобы убедиться, что это тело содержит хотя бы один пустой абзац.
body.ensure_minimum()
# Теперь мы можем добавить run'ы в тело и заставить документ отобразить их.
body.first_paragraph.append_child(aw.Run(doc=doc, text='Hello world!'))
self.assertEqual('Hello world!', doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [Section](../)

