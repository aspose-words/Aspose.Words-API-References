---
title: ListLabel.label_string property
linktitle: label_string property
articleTitle: label_string property
second_title: Aspose.Words for Python
description: "ListLabel.label_string property. Gets a string representation of list label."
type: docs
weight: 20
url: /de/python-net/aspose.words.lists/listlabel/label_string/
---

## ListLabel.label_string property

Gets a string representation of list label.


```python
@property
def label_string(self) -> str:
    ...

```

### Examples

Shows how to extract the list labels of all paragraphs that are list items.

```python
doc = aw.Document(file_name=MY_DIR + 'Rendering.docx')
doc.update_list_labels()
paras = doc.get_child_nodes(aw.NodeType.PARAGRAPH, True)
# Finden Sie heraus, ob wir die Absatzliste haben. In unserem Dokument verwendet unsere Liste einfache arabische Zahlen,
# die bei drei beginnen und bei sechs enden.
for paragraph in list(filter(lambda p: p.list_format.is_list_item, list(filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_paragraph(), b), list(paras)))))):
    print(f'List item paragraph #{paras.index_of(paragraph)}')
    # Dies ist der Text, den wir erhalten, wenn wir diesen Knoten im Textformat ausgeben.
    # Diese Textausgabe lässt Listeneinträge weg. Entfernen Sie alle Absatzformatierungszeichen.
    paragraph_text = paragraph.to_string(save_format=aw.SaveFormat.TEXT).strip()
    print(f'\tExported Text: {paragraph_text}')
    label = paragraph.list_label
    # Dies ermittelt die Position des Absatzes in der aktuellen Ebene der Liste. Wenn wir eine Liste mit mehreren Ebenen haben,
    # wird uns sagen, welche Position es auf dieser Ebene hat.
    print(f'\tNumerical Id: {label.label_value}')
    # Kombinieren Sie sie, um das Listenelement zusammen mit dem Text in der Ausgabe einzuschließen.
    print(f'\tList label combined with text: {label.label_string} {paragraph_text}')
```

### See Also

* module [aspose.words.lists](../../)
* class [ListLabel](../)

