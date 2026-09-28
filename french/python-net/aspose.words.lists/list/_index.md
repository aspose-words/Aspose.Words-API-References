---
title: List class
linktitle: List class
articleTitle: List class
second_title: Aspose.Words for Python
description: "aspose.words.lists.List class. Represents formatting of a list"
type: docs
weight: 10
url: /fr/python-net/aspose.words.lists/list/
---

## List class

Represents formatting of a list.
To learn more, visit the [Working with Lists](https://docs.aspose.com/words/python-net/working-with-lists/) documentation article.




### Remarks

A list in a Microsoft Word document is a set of list formatting properties.
Each list can have up to 9 levels and formatting properties, such as number style, start value,
indent, tab position etc are defined separately for each level.

A [List](./) object always belongs to the [ListCollection](../listcollection/) collection.

To create a new list, use the Add methods of the [ListCollection](../listcollection/) collection.

To modify formatting of a list, use [ListLevel](../listlevel/) objects found in
the [List.list_levels](./list_levels/) collection.

To apply or remove list formatting from a paragraph, use [ListFormat](../listformat/).




### Properties

| Name | Description |
| --- | --- |
| [document](./document/) | Gets the owner document. |
| [is_list_style_definition](./is_list_style_definition/) | Returns ``True`` if this list is a definition of a list style. |
| [is_list_style_reference](./is_list_style_reference/) | Returns ``True`` if this list is a reference to a list style. |
| [is_multi_level](./is_multi_level/) | Returns ``True`` when the list contains 9 levels; ``False`` when 1 level. |
| [is_restart_at_each_section](./is_restart_at_each_section/) | Specifies whether list should be restarted at each section. Default value is ``False``. |
| [list_id](./list_id/) | Gets the unique identifier of the list. |
| [list_levels](./list_levels/) | Gets the collection of list levels for this list. |
| [style](./style/) | Gets the list style that this list references or defines. |

### Methods

| Name | Description |
| --- | --- |
|[ compare_to(obj)](./compare_to/#object) | Compares the specified object to the current object. |
|[ compare_to(other)](./compare_to/#list) | Compares the specified list to the current list. |
|[ equals(list)](./equals/#list) | Compares with the specified list. |
|[ has_same_template(other)](./has_same_template/#list) | Returns true if the current list and the given list are created from the same template. |

### Examples

Shows how to work with list levels.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
self.assertFalse(builder.list_format.is_list_item)
# Une liste nous permet d'organiser et de décorer des ensembles de paragraphes avec des symboles préfixes et des retraits.
# Nous pouvons créer des listes imbriquées en augmentant le niveau de retrait.
# Nous pouvons commencer et terminer une liste en utilisant la propriété "ListFormat" d'un constructeur de document.
# Chaque paragraphe que nous ajoutons entre le début et la fin d'une liste deviendra un élément de la liste.
# Ci-dessous se trouvent deux types de listes que nous pouvons créer à l'aide d'un constructeur de document.
# 1 -  Une liste numérotée :
# Les listes numérotées créent un ordre logique pour leurs paragraphes en numérotant chaque élément.
builder.list_format.list = doc.lists.add(list_template=aw.lists.ListTemplate.NUMBER_DEFAULT)
self.assertTrue(builder.list_format.is_list_item)
# En définissant la propriété "ListLevelNumber", nous pouvons augmenter le niveau de la liste
# pour commencer une sous-liste autonome à l'élément de liste actuel.
# Le modèle de liste Microsoft Word appelé "NumberDefault" utilise des chiffres pour créer des niveaux de liste pour le premier niveau de liste.
# Les niveaux de liste plus profonds utilisent des lettres et des chiffres romains minuscules.
i = 0
while i < 9:
    builder.list_format.list_level_number = i
    builder.writeln('Level ' + str(i))
    i += 1
# 2 -  Une liste à puces :
# Cette liste appliquera un retrait et un symbole de puce ("•") avant chaque paragraphe.
# Les niveaux plus profonds de cette liste utiliseront différents symboles, tels que "■" et "○".
builder.list_format.list = doc.lists.add(list_template=aw.lists.ListTemplate.BULLET_DEFAULT)
i = 0
while i < 9:
    builder.list_format.list_level_number = i
    builder.writeln('Level ' + str(i))
    i += 1
# Nous pouvons désactiver le formatage de liste pour ne pas formater les paragraphes suivants comme des listes en désactivant le drapeau "List".
builder.list_format.list = None
self.assertFalse(builder.list_format.is_list_item)
doc.save(file_name=ARTIFACTS_DIR + 'Lists.SpecifyListLevel.docx')
```

Shows how to apply custom list formatting to paragraphs when using DocumentBuilder.

```python
doc = aw.Document()
# Une liste nous permet d'organiser et de décorer des ensembles de paragraphes avec des symboles préfixes et des retraits.
# Nous pouvons créer des listes imbriquées en augmentant le niveau de retrait.
# Nous pouvons commencer et terminer une liste en utilisant la propriété "ListFormat" d'un constructeur de document.
# Chaque paragraphe que nous ajoutons entre le début et la fin d'une liste deviendra un élément de la liste.
# Créez une liste à partir d'un modèle Microsoft Word et personnalisez les deux premiers niveaux de sa liste.
doc_list = doc.lists.add(list_template=aw.lists.ListTemplate.NUMBER_DEFAULT)
list_level = doc_list.list_levels[0]
list_level.font.color = aspose.pydrawing.Color.red
list_level.font.size = 24
list_level.number_style = aw.NumberStyle.ORDINAL_TEXT
list_level.start_at = 21
list_level.number_format = '\x00'
list_level.number_position = -36
list_level.text_position = 144
list_level.tab_position = 144
list_level = doc_list.list_levels[1]
list_level.alignment = aw.lists.ListLevelAlignment.RIGHT
list_level.number_style = aw.NumberStyle.BULLET
list_level.font.name = 'Wingdings'
list_level.font.color = aspose.pydrawing.Color.blue
list_level.font.size = 24
# Cette valeur NumberFormat créera des symboles de puces en forme d'étoile.
list_level.number_format = '\uf0af'
list_level.trailing_character = aw.lists.ListTrailingCharacter.SPACE
list_level.number_position = 144
# Créez des paragraphes et appliquez les deux niveaux de liste de notre formatage de liste personnalisé à ceux-ci.
builder = aw.DocumentBuilder(doc=doc)
builder.list_format.list = doc_list
builder.writeln('The quick brown fox...')
builder.writeln('The quick brown fox...')
builder.list_format.list_indent()
builder.writeln('jumped over the lazy dog.')
builder.writeln('jumped over the lazy dog.')
builder.list_format.list_outdent()
builder.writeln('The quick brown fox...')
builder.list_format.remove_numbers()
builder.document.save(file_name=ARTIFACTS_DIR + 'Lists.CreateCustomList.docx')
```

Shows how to restart numbering in a list by copying a list.

```python
doc = aw.Document()
# Une liste nous permet d'organiser et de décorer des ensembles de paragraphes avec des symboles préfixes et des retraits.
# Nous pouvons créer des listes imbriquées en augmentant le niveau de retrait.
# Nous pouvons commencer et terminer une liste en utilisant la propriété "ListFormat" d'un constructeur de document.
# Chaque paragraphe que nous ajoutons entre le début et la fin d'une liste deviendra un élément de la liste.
# Créez une liste à partir d'un modèle Microsoft Word et personnalisez son premier niveau de liste.
list1 = doc.lists.add(list_template=aw.lists.ListTemplate.NUMBER_ARABIC_PARENTHESIS)
list1.list_levels[0].font.color = aspose.pydrawing.Color.red
list1.list_levels[0].alignment = aw.lists.ListLevelAlignment.RIGHT
# Appliquez notre liste à certains paragraphes.
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('List 1 starts below:')
builder.list_format.list = list1
builder.writeln('Item 1')
builder.writeln('Item 2')
builder.list_format.remove_numbers()
# Nous pouvons ajouter une copie d'une liste existante à la collection de listes du document
# pour créer une liste similaire sans modifier l'original.
list2 = doc.lists.add_copy(list1)
list2.list_levels[0].font.color = aspose.pydrawing.Color.blue
list2.list_levels[0].start_at = 10
# Appliquez la deuxième liste aux nouveaux paragraphes.
builder.writeln('List 2 starts below:')
builder.list_format.list = list2
builder.writeln('Item 1')
builder.writeln('Item 2')
builder.list_format.remove_numbers()
doc.save(file_name=ARTIFACTS_DIR + 'Lists.RestartNumberingUsingListCopy.docx')
```

### See Also

* module [aspose.words.lists](../)
* class [ListCollection](../listcollection/)
* class [ListLevel](../listlevel/)
* class [ListFormat](../listformat/)

