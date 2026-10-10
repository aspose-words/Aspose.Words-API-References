---
title: ListLabel.label_value property
linktitle: label_value property
articleTitle: label_value property
second_title: Aspose.Words for Python
description: "ListLabel.label_value property. Gets a numeric value for this label."
type: docs
weight: 30
url: /it/python-net/aspose.words.lists/listlabel/label_value/
---

## ListLabel.label_value property

Gets a numeric value for this label.


```python
@property
def label_value(self) -> int:
    ...

```

### Remarks

Use the [Document.update_list_labels()](../../../aspose.words/document/update_list_labels/#default) method to update the value of this property.



### Examples

Shows how to extract the list labels of all paragraphs that are list items.

```python
doc = aw.Document(file_name=MY_DIR + 'Rendering.docx')
doc.update_list_labels()
paras = doc.get_child_nodes(aw.NodeType.PARAGRAPH, True)
# Trova se abbiamo l'elenco dei paragrafi. Nel nostro documento, il nostro elenco utilizza numeri arabi semplici,
# che inizia da tre e termina a sei.
for paragraph in list(filter(lambda p: p.list_format.is_list_item, list(filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_paragraph(), b), list(paras)))))):
    print(f'List item paragraph #{paras.index_of(paragraph)}')
    # Questo è il testo che otteniamo quando esportiamo questo nodo in formato testo.
    # Questa uscita di testo ometterà le etichette dell'elenco. Rimuovi eventuali caratteri di formattazione dei paragrafi.
    paragraph_text = paragraph.to_string(save_format=aw.SaveFormat.TEXT).strip()
    print(f'\tExported Text: {paragraph_text}')
    label = paragraph.list_label
    # Questo ottiene la posizione del paragrafo nel livello corrente dell'elenco. Se abbiamo un elenco con più livelli,
    # ci dirà qual è la sua posizione in quel livello.
    print(f'\tNumerical Id: {label.label_value}')
    # Combinali insieme per includere l'etichetta dell'elenco con il testo nell'output.
    print(f'\tList label combined with text: {label.label_string} {paragraph_text}')
```

### See Also

* module [aspose.words.lists](../../)
* class [ListLabel](../)

