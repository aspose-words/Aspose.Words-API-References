---
title: StyleCollection.add method
linktitle: add method
articleTitle: add method
second_title: Aspose.Words for Python
description: "StyleCollection.add method. Creates a new user defined style and adds it the collection."
type: docs
weight: 60
url: /it/python-net/aspose.words/stylecollection/add/
---

## add(type, name) {#styletype_str}

Creates a new user defined style and adds it the collection.


```python
def add(self, type: aspose.words.StyleType, name: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| type | [StyleType](../../styletype/) | A [StyleType](../../styletype/) value that specifies the type of the style to create. |
| name | str | Case sensitive name of the style to create. |

### Remarks

You can create character, paragraph or a list style.

When creating a list style, the style is created with default numbered list formatting (1 \\ a \\ i).

Throws an exception if a style with this name already exists.




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

Shows how to add a Style to a document's styles collection.

```python
doc = aw.Document()
styles = doc.styles
# Imposta i parametri predefiniti per i nuovi stili che potremmo aggiungere in seguito a questa raccolta.
styles.default_font.name = 'Courier New'
# Se aggiungiamo uno stile di tipo "StyleType.Paragraph", la raccolta applicherà i valori di
# la sua proprietà "DefaultParagraphFormat" allo "ParagraphFormat" dello stile.
styles.default_paragraph_format.first_line_indent = 15
# Aggiungi uno stile, quindi verifica che abbia le impostazioni predefinite.
styles.add(aw.StyleType.PARAGRAPH, 'MyStyle')
self.assertEqual('Courier New', styles[4].font.name)
self.assertEqual(15, styles.get_by_name('MyStyle').paragraph_format.first_line_indent)
```

### See Also

* module [aspose.words](../../)
* class [StyleCollection](../)

