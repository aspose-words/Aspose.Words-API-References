---
title: List.is_multi_level property
linktitle: is_multi_level property
articleTitle: is_multi_level property
second_title: Aspose.Words for Python
description: "List.is_multi_level property. Returns ``True`` when the list contains 9 levels; ``False`` when 1 level."
type: docs
weight: 40
url: /fr/python-net/aspose.words.lists/list/is_multi_level/
---

## List.is_multi_level property

Returns ``True`` when the list contains 9 levels; ``False`` when 1 level.



```python
@property
def is_multi_level(self) -> bool:
    ...

```

### Remarks

The lists that you create with Aspose.Words are always multi-level lists and contain 9 levels.

Microsoft Word 2003 and later always create multi-level lists with 9 levels.
But in some documents, created with earlier versions of Microsoft Word you might encounter
lists that have 1 level only.




### Examples

Shows how to create a list style and use it in a document.

```python
doc = aw.Document()
# Une liste nous permet d'organiser et de décorer des ensembles de paragraphes avec des symboles préfixes et des retraits.
# Nous pouvons créer des listes imbriquées en augmentant le niveau de retrait.
# Nous pouvons commencer et terminer une liste en utilisant la propriété "ListFormat" d'un constructeur de document.
# Chaque paragraphe que nous ajoutons entre le début et la fin d'une liste deviendra un élément de la liste.
# Nous pouvons contenir un objet List complet au sein d'un style.
list_style = doc.styles.add(aw.StyleType.LIST, 'MyListStyle')
list1 = list_style.list
self.assertTrue(list1.is_list_style_definition)
self.assertFalse(list1.is_list_style_reference)
self.assertTrue(list1.is_multi_level)
self.assertEqual(list_style, list1.style)
# Modifiez l'apparence de tous les niveaux de liste dans notre liste.
for level in list1.list_levels:
    level.font.name = 'Verdana'
    level.font.color = aspose.pydrawing.Color.blue
    level.font.bold = True
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Using list style first time:')
# Créez une autre liste à partir d'une liste dans un style.
list2 = doc.lists.add(list_style=list_style)
self.assertFalse(list2.is_list_style_definition)
self.assertTrue(list2.is_list_style_reference)
self.assertEqual(list_style, list2.style)
# Ajoutez des éléments de liste que notre liste formattera.
builder.list_format.list = list2
builder.writeln('Item 1')
builder.writeln('Item 2')
builder.list_format.remove_numbers()
builder.writeln('Using list style second time:')
# Créez et appliquez une autre liste basée sur le style de liste.
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

