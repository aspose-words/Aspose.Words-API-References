---
title: ListFormat.apply_bullet_default method
linktitle: apply_bullet_default method
articleTitle: apply_bullet_default method
second_title: Aspose.Words for Python
description: "ListFormat.apply_bullet_default method. Starts a new default bulleted list and applies it to the paragraph."
type: docs
weight: 50
url: /fr/python-net/aspose.words.lists/listformat/apply_bullet_default/
---

## apply_bullet_default() {#default}

Starts a new default bulleted list and applies it to the paragraph.


```python
def apply_bullet_default(self):
    ...
```

### Remarks

This is a shortcut method that creates a new list using the default bulleted
template, applies it to the paragraph and selects the 1st list level.




### Examples

Shows how to create bulleted and numbered lists.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Aspose.Words main advantages are:')
# Une liste nous permet d'organiser et de décorer des ensembles de paragraphes avec des symboles préfixes et des retraits.
# Nous pouvons créer des listes imbriquées en augmentant le niveau de retrait.
# Nous pouvons commencer et terminer une liste en utilisant la propriété "ListFormat" d'un constructeur de document.
# Chaque paragraphe que nous ajoutons entre le début et la fin d'une liste deviendra un élément de la liste.
# Ci-dessous, deux types de listes que nous pouvons créer avec un constructeur de document.
# 1 -  Une liste à puces :
# Cette liste appliquera un retrait et un symbole de puce ("•") avant chaque paragraphe.
builder.list_format.apply_bullet_default()
builder.writeln('Great performance')
builder.writeln('High reliability')
builder.writeln('Quality code and working')
builder.writeln('Wide variety of features')
builder.writeln('Easy to understand API')
# Terminez la liste à puces.
builder.list_format.remove_numbers()
builder.insert_break(aw.BreakType.PARAGRAPH_BREAK)
builder.writeln('Aspose.Words allows:')
# 2 -  Une liste numérotée :
# Les listes numérotées créent un ordre logique pour leurs paragraphes en numérotant chaque élément.
builder.list_format.apply_number_default()
# Ce paragraphe est le premier élément. Le premier élément d'une liste numérotée aura un "1." comme symbole d'élément de liste.
builder.writeln('Opening documents from different formats:')
self.assertEqual(0, builder.list_format.list_level_number)
# Appelez la méthode "ListIndent" pour augmenter le niveau de liste actuel,
# ce qui démarrera une nouvelle liste autonome, avec une indentation plus profonde, à l'élément actuel du premier niveau de liste.
builder.list_format.list_indent()
self.assertEqual(1, builder.list_format.list_level_number)
# Voici les trois premiers éléments de liste du deuxième niveau de liste, qui maintiendront un compte
# indépendant du compte du premier niveau de liste. Selon le format de liste actuel,
# ils auront les symboles "a.", "b.", et "c.".
builder.writeln('DOC')
builder.writeln('PDF')
builder.writeln('HTML')
# Appelez la méthode "ListOutdent" pour revenir au niveau de liste précédent.
builder.list_format.list_outdent()
self.assertEqual(0, builder.list_format.list_level_number)
# Ces deux paragraphes continueront le compte du premier niveau de liste.
# Ces éléments auront les symboles "2.", et "3."
builder.writeln('Processing documents')
builder.writeln('Saving documents in different formats:')
# Si nous augmentons le niveau de liste à un niveau auquel nous avons déjà ajouté des éléments,
# la liste imbriquée sera séparée de la précédente, et sa numérotation commencera depuis le début.
# Ces éléments de liste auront les symboles "a.", "b.", "c.", "d.", et "e".
builder.list_format.list_indent()
builder.writeln('DOC')
builder.writeln('PDF')
builder.writeln('HTML')
builder.writeln('MHTML')
builder.writeln('Plain text')
# Désindentez à nouveau le niveau de la liste.
builder.list_format.list_outdent()
builder.writeln('Doing many other things!')
# Terminez la liste numérotée.
builder.list_format.remove_numbers()
doc.save(file_name=ARTIFACTS_DIR + 'Lists.ApplyDefaultBulletsAndNumbers.docx')
```

### See Also

* module [aspose.words.lists](../../)
* class [ListFormat](../)
* property [ListFormat.list](../list/)
* method [ListFormat.remove_numbers()](../remove_numbers/#default)
* property [ListFormat.list_level_number](../list_level_number/)

