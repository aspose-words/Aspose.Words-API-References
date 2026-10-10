---
title: List.is_list_style_reference property
linktitle: is_list_style_reference property
articleTitle: is_list_style_reference property
second_title: Aspose.Words for Python
description: "List.is_list_style_reference property. Returns ``True`` if this list is a reference to a list style."
type: docs
weight: 30
url: /de/python-net/aspose.words.lists/list/is_list_style_reference/
---

## List.is_list_style_reference property

Returns ``True`` if this list is a reference to a list style.



```python
@property
def is_list_style_reference(self) -> bool:
    ...

```

### Remarks

Note, modifying properties of a list that is a reference to list style has no effect.
The list formatting specified in the list style itself always takes precedence.




### Examples

Shows how to create a list style and use it in a document.

```python
doc = aw.Document()
# Eine Liste ermöglicht es uns, Satzgruppen von Absätzen mit Präfixsymbolen und Einzügen zu organisieren und zu dekorieren.
# Wir können verschachtelte Listen erstellen, indem wir die Einzugsebene erhöhen.
# Wir können eine Liste beginnen und beenden, indem wir die "ListFormat"-Eigenschaft eines Document Builders verwenden.
# Jeder Absatz, den wir zwischen dem Beginn und dem Ende einer Liste hinzufügen, wird zu einem Element der Liste.
# Wir können ein komplettes List-Objekt in einem Stil enthalten.
list_style = doc.styles.add(aw.StyleType.LIST, 'MyListStyle')
list1 = list_style.list
self.assertTrue(list1.is_list_style_definition)
self.assertFalse(list1.is_list_style_reference)
self.assertTrue(list1.is_multi_level)
self.assertEqual(list_style, list1.style)
# Ändern Sie das Aussehen aller Listenebenen in unserer Liste.
for level in list1.list_levels:
    level.font.name = 'Verdana'
    level.font.color = aspose.pydrawing.Color.blue
    level.font.bold = True
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Using list style first time:')
# Erstellen Sie eine weitere Liste aus einer Liste innerhalb eines Stils.
list2 = doc.lists.add(list_style=list_style)
self.assertFalse(list2.is_list_style_definition)
self.assertTrue(list2.is_list_style_reference)
self.assertEqual(list_style, list2.style)
# Fügen Sie einige Listenelemente hinzu, die unsere Liste formatieren wird.
builder.list_format.list = list2
builder.writeln('Item 1')
builder.writeln('Item 2')
builder.list_format.remove_numbers()
builder.writeln('Using list style second time:')
# Erstellen und wenden Sie eine weitere Liste basierend auf dem Liststil an.
list3 = doc.lists.add(list_style=list_style)
builder.list_format.list = list3
builder.writeln('Item 1')
builder.writeln('Item 2')
builder.list_format.remove_numbers()
builder.document.save(file_name=ARTIFACTS_DIR + 'Lists.CreateAndUseListStyle.docx')
```

### See Also

* module [aspose.words.lists](../../)
* class [List](../)
* property [List.style](../style/)
* property [List.is_list_style_definition](../is_list_style_definition/)

