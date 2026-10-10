---
title: DocumentBase.lists property
linktitle: lists property
articleTitle: lists property
second_title: Aspose.Words for Python
description: "DocumentBase.lists property. Provides access to the list formatting used in the document."
type: docs
weight: 50
url: /fr/python-net/aspose.words/documentbase/lists/
---

## DocumentBase.lists property

Provides access to the list formatting used in the document.


```python
@property
def lists(self) -> aspose.words.lists.ListCollection:
    ...

```

### Remarks

For more information see the description of the [ListCollection](../../../aspose.words.lists/listcollection/) class.




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

### See Also

* module [aspose.words](../../)
* class [DocumentBase](../)
* class [ListCollection](../../../aspose.words.lists/listcollection/)
* class [List](../../../aspose.words.lists/list/)
* class [ListFormat](../../../aspose.words.lists/listformat/)

