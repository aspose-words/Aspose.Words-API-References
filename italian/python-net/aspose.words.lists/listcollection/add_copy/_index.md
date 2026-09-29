---
title: ListCollection.add_copy method
linktitle: add_copy method
articleTitle: add_copy method
second_title: Aspose.Words for Python
description: "ListCollection.add_copy method. Creates a new list by copying the specified list and adding it to the collection of lists in the document."
type: docs
weight: 50
url: /it/python-net/aspose.words.lists/listcollection/add_copy/
---

## add_copy(src_list) {#list}

Creates a new list by copying the specified list and adding it to the collection of lists in the document.


```python
def add_copy(self, src_list: aspose.words.lists.List):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| src_list | [List](../../list/) | The source list to copy from. |

### Remarks

The source list can be from any document. If the source list belongs to a different document,
a copy of the list is created and added to the current document.

If the source list is a reference to or a definition of a list style,
the newly created list is not related to the original list style.




### Returns

The newly created list.


### Examples

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

Shows how to create a document with a sample of all the lists from another document.

```python
src_doc = aw.Document(file_name=MY_DIR + 'Rendering.docx')
dst_doc = aw.Document()
builder = aw.DocumentBuilder(doc=dst_doc)
for src_list in src_doc.lists:
    dst_list = dst_doc.lists.add_copy(src_list)
    ExLists._add_list_sample(builder, dst_list)
dst_doc.save(file_name=ARTIFACTS_DIR + 'Lists.PrintOutAllLists.docx')
```

Shows how to create a document with a sample of all the lists from another document (AddListSample).

```python
@staticmethod
def _add_list_sample(builder, doc_list):
    builder.writeln('Sample formatting of list with ListId:' + str(doc_list.list_id))
    builder.list_format.list = doc_list
    i = 0
    while i < doc_list.list_levels.count:
        builder.list_format.list_level_number = i
        builder.writeln('Level ' + str(i))
        i += 1
    builder.list_format.remove_numbers()
    builder.writeln()
```

### See Also

* module [aspose.words.lists](../../)
* class [ListCollection](../)

