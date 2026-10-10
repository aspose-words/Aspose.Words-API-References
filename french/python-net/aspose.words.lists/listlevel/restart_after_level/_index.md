---
title: ListLevel.restart_after_level property
linktitle: restart_after_level property
articleTitle: restart_after_level property
second_title: Aspose.Words for Python
description: "ListLevel.restart_after_level property. Sets or returns the list level that must appear before the specified list level restarts numbering."
type: docs
weight: 100
url: /fr/python-net/aspose.words.lists/listlevel/restart_after_level/
---

## ListLevel.restart_after_level property

Sets or returns the list level that must appear before the specified list level restarts numbering.


```python
@property
def restart_after_level(self) -> int:
    ...

@restart_after_level.setter
def restart_after_level(self, value: int):
    ...

```

### Remarks

The value of -1 means the numbering will continue.




### Examples

Shows advances ways of customizing list labels.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Une liste nous permet d'organiser et de décorer des ensembles de paragraphes avec des symboles préfixes et des retraits.
# Nous pouvons créer des listes imbriquées en augmentant le niveau de retrait.
# Nous pouvons commencer et terminer une liste en utilisant la propriété "ListFormat" d'un constructeur de document.
# Chaque paragraphe que nous ajoutons entre le début et la fin d'une liste deviendra un élément de la liste.
doc_list = doc.lists.add(list_template=aw.lists.ListTemplate.NUMBER_DEFAULT)
# Les libellés de niveau 1 seront formatés selon le style de paragraphe "Heading 1" et auront un préfixe.
# Ils ressembleront à "Appendix A", "Appendix B"...
doc_list.list_levels[0].number_format = 'Appendix \x00'
doc_list.list_levels[0].number_style = aw.NumberStyle.UPPERCASE_LETTER
doc_list.list_levels[0].linked_style = doc.styles.get_by_name('Heading 1')
# Les libellés de niveau 2 afficheront les numéros actuels du premier et du deuxième niveau de liste et auront des zéros initiaux.
# Si le premier niveau de liste est à 1, alors les libellés de ces listes ressembleront à "Section (1.01)", "Section (1.02)"...
doc_list.list_levels[1].number_format = 'Section (\x00.\x01)'
doc_list.list_levels[1].number_style = aw.NumberStyle.LEADING_ZERO
# Notez que le niveau supérieur utilise la numérotation UppercaseLetter.
# Nous pouvons définir la propriété "IsLegal" pour utiliser des chiffres arabes pour les niveaux de liste supérieurs.
doc_list.list_levels[1].is_legal = True
doc_list.list_levels[1].restart_after_level = 0
# Les libellés de niveau 3 seront des chiffres romains majuscules avec un préfixe et un suffixe et redémarreront à chaque élément de niveau 1 de la liste.
# Ces libellés de liste ressembleront à "-I-", "-II-"...
doc_list.list_levels[2].number_format = '-\x02-'
doc_list.list_levels[2].number_style = aw.NumberStyle.UPPERCASE_ROMAN
doc_list.list_levels[2].restart_after_level = 1
# Rendez les libellés de tous les niveaux de liste en gras.
for level in doc_list.list_levels:
    level.font.bold = True
# Appliquez le formatage de liste au paragraphe actuel.
builder.list_format.list = doc_list
# Créez des éléments de liste qui afficheront les trois niveaux de notre liste.
n = 0
while n < 2:
    i = 0
    while i < 3:
        builder.list_format.list_level_number = i
        builder.writeln('Level ' + str(i))
        i += 1
    n += 1
builder.list_format.remove_numbers()
doc.save(file_name=ARTIFACTS_DIR + 'Lists.CreateListRestartAfterHigher.docx')
```

### See Also

* module [aspose.words.lists](../../)
* class [ListLevel](../)

