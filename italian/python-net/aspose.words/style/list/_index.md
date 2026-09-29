---
title: Style.list property
linktitle: list property
articleTitle: list property
second_title: Aspose.Words for Python
description: "Style.list property. Gets the list that defines formatting of this list style."
type: docs
weight: 100
url: /it/python-net/aspose.words/style/list/
---

## Style.list property

Gets the list that defines formatting of this list style.


```python
@property
def list(self) -> aspose.words.lists.List:
    ...

```

### Remarks

This property is only valid for list styles.
For other style types this property returns ``None``.




### Examples

Shows how to create a list style and use it in a document.

```python
doc = aw.Document()
# Un elenco ci consente di organizzare e decorare insiemi di paragrafi con simboli prefisso e rientri.
# Possiamo creare elenchi nidificati aumentando il livello di rientro.
# Possiamo iniziare e terminare un elenco usando la proprietà \"ListFormat\" di un document builder.
# Ogni paragrafo che aggiungiamo tra l'inizio e la fine di un elenco diventerà un elemento dell'elenco.
# Possiamo contenere un intero oggetto List all'interno di uno stile.
list_style = doc.styles.add(aw.StyleType.LIST, 'MyListStyle')
list1 = list_style.list
self.assertTrue(list1.is_list_style_definition)
self.assertFalse(list1.is_list_style_reference)
self.assertTrue(list1.is_multi_level)
self.assertEqual(list_style, list1.style)
# Modifica l'aspetto di tutti i livelli dell'elenco nel nostro elenco.
for level in list1.list_levels:
    level.font.name = 'Verdana'
    level.font.color = aspose.pydrawing.Color.blue
    level.font.bold = True
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Using list style first time:')
# Crea un altro elenco da un elenco all'interno di uno stile.
list2 = doc.lists.add(list_style=list_style)
self.assertFalse(list2.is_list_style_definition)
self.assertTrue(list2.is_list_style_reference)
self.assertEqual(list_style, list2.style)
# Aggiungi alcuni elementi dell'elenco che il nostro elenco formatterà.
builder.list_format.list = list2
builder.writeln('Item 1')
builder.writeln('Item 2')
builder.list_format.remove_numbers()
builder.writeln('Using list style second time:')
# Crea e applica un altro elenco basato sullo stile dell'elenco.
list3 = doc.lists.add(list_style=list_style)
builder.list_format.list = list3
builder.writeln('Item 1')
builder.writeln('Item 2')
builder.list_format.remove_numbers()
builder.document.save(file_name=ARTIFACTS_DIR + 'Lists.CreateAndUseListStyle.docx')
```

### See Also

* module [aspose.words](../../)
* class [Style](../)

