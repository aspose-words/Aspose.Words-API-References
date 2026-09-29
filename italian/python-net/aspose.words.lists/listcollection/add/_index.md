---
title: ListCollection.add method
linktitle: add method
articleTitle: add method
second_title: Aspose.Words for Python
description: "aspose.words.lists.ListCollection.add method"
type: docs
weight: 40
url: /it/python-net/aspose.words.lists/listcollection/add/
---

## add(list_template) {#listtemplate}

Creates a new list based on a predefined template and adds it to the collection of lists in the document.


```python
def add(self, list_template: aspose.words.lists.ListTemplate):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| list_template | [ListTemplate](../../listtemplate/) | The template of the list. |

### Remarks

Aspose.Words list templates correspond to the 21 list templates available
in the Bullets and Numbering dialog box in Microsoft Word 2003.

All lists created using this method have 9 list levels.




### Returns

The newly created list.


## add(list_style) {#style}

Creates a new list that references a list style and adds it to the collection of lists in the document.


```python
def add(self, list_style: aspose.words.Style):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| list_style | [Style](../../../aspose.words/style/) | The list style. |

### Remarks

The newly created list references the list style. If you change the properties of the list
style, it is reflected in the properties of the list. Vice versa, if you change the properties
of the list, it is reflected in the properties of the list style.




### Returns

The newly created list.


## Examples

Shows how to work with list levels.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
self.assertFalse(builder.list_format.is_list_item)
# Un elenco ci consente di organizzare e decorare insiemi di paragrafi con simboli prefisso e rientri.
# Possiamo creare elenchi nidificati aumentando il livello di rientro.
# Possiamo iniziare e terminare un elenco usando la proprietà \"ListFormat\" di un document builder.
# Ogni paragrafo che aggiungiamo tra l'inizio e la fine di un elenco diventerà un elemento dell'elenco.
# Di seguito sono riportati due tipi di elenchi che possiamo creare usando un document builder.
# 1 -  Un elenco numerato:
# Gli elenchi numerati creano un ordine logico per i loro paragrafi numerando ogni elemento.
builder.list_format.list = doc.lists.add(list_template=aw.lists.ListTemplate.NUMBER_DEFAULT)
self.assertTrue(builder.list_format.is_list_item)
# Impostando la proprietà \"ListLevelNumber\", possiamo aumentare il livello dell'elenco
# per avviare un sottoelenco autonomo all'elemento corrente dell'elenco.
# Il modello di elenco di Microsoft Word chiamato \"NumberDefault\" utilizza numeri per creare livelli di elenco per il primo livello.
# I livelli di elenco più profondi usano lettere e numeri romani minuscoli.
i = 0
while i < 9:
    builder.list_format.list_level_number = i
    builder.writeln('Level ' + str(i))
    i += 1
# 2 -  Un elenco puntato:
# Questo elenco applicherà un rientro e un simbolo di punto elenco (\"•\") prima di ogni paragrafo.
# I livelli più profondi di questo elenco utilizzeranno simboli diversi, come \"■\" e \"○\".
builder.list_format.list = doc.lists.add(list_template=aw.lists.ListTemplate.BULLET_DEFAULT)
i = 0
while i < 9:
    builder.list_format.list_level_number = i
    builder.writeln('Level ' + str(i))
    i += 1
# Possiamo disabilitare la formattazione degli elenchi per non formattare i paragrafi successivi come elenchi rimuovendo il flag \"List\".
builder.list_format.list = None
self.assertFalse(builder.list_format.is_list_item)
doc.save(file_name=ARTIFACTS_DIR + 'Lists.SpecifyListLevel.docx')
```

Shows how to restart numbering in a list by copying a list.

```python
doc = aw.Document()
# Un elenco ci consente di organizzare e decorare insiemi di paragrafi con simboli prefisso e rientri.
# Possiamo creare elenchi nidificati aumentando il livello di rientro.
# Possiamo iniziare e terminare un elenco usando la proprietà \"ListFormat\" di un document builder.
# Ogni paragrafo che aggiungiamo tra l'inizio e la fine di un elenco diventerà un elemento dell'elenco.
# Crea un elenco da un modello di Microsoft Word e personalizza il suo primo livello di elenco.
list1 = doc.lists.add(list_template=aw.lists.ListTemplate.NUMBER_ARABIC_PARENTHESIS)
list1.list_levels[0].font.color = aspose.pydrawing.Color.red
list1.list_levels[0].alignment = aw.lists.ListLevelAlignment.RIGHT
# Applica il nostro elenco a qualche paragrafo.
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('List 1 starts below:')
builder.list_format.list = list1
builder.writeln('Item 1')
builder.writeln('Item 2')
builder.list_format.remove_numbers()
# Possiamo aggiungere una copia di un elenco esistente alla collezione di elenchi del documento
# per creare un elenco simile senza apportare modifiche all'originale.
list2 = doc.lists.add_copy(list1)
list2.list_levels[0].font.color = aspose.pydrawing.Color.blue
list2.list_levels[0].start_at = 10
# Applica il secondo elenco a nuovi paragrafi.
builder.writeln('List 2 starts below:')
builder.list_format.list = list2
builder.writeln('Item 1')
builder.writeln('Item 2')
builder.list_format.remove_numbers()
doc.save(file_name=ARTIFACTS_DIR + 'Lists.RestartNumberingUsingListCopy.docx')
```

Shows how to create a list by applying a new list format to a collection of paragraphs.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Paragraph 1')
builder.writeln('Paragraph 2')
builder.write('Paragraph 3')
paras = doc.get_child_nodes(aw.NodeType.PARAGRAPH, True)
self.assertEqual(0, len(list(filter(lambda n: n.as_paragraph().list_format.is_list_item, paras))))
doc_list = doc.lists.add(list_template=aw.lists.ListTemplate.NUMBER_UPPERCASE_LETTER_DOT)
for paragraph in filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_paragraph(), b), list(paras))):
    paragraph.list_format.list = doc_list
    paragraph.list_format.list_level_number = 1
self.assertEqual(3, len(list(filter(lambda n: n.as_paragraph().list_format.is_list_item, paras))))
```

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

## See Also

* module [aspose.words.lists](../../)
* class [ListCollection](../)

