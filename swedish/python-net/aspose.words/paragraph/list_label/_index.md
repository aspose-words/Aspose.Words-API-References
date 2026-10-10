---
title: Paragraph.list_label property
linktitle: list_label property
articleTitle: list_label property
second_title: Aspose.Words for Python
description: "Paragraph.list_label property. Gets a [Paragraph.list_label](./) object that provides access to list numbering value and formatting for this paragraph."
type: docs
weight: 160
url: /sv/python-net/aspose.words/paragraph/list_label/
---

## Paragraph.list_label property

Gets a [Paragraph.list_label](./) object that provides access to list numbering value and formatting
for this paragraph.



```python
@property
def list_label(self) -> aspose.words.lists.ListLabel:
    ...

```

### Examples

Shows how to extract the list labels of all paragraphs that are list items.

```python
doc = aw.Document(file_name=MY_DIR + 'Rendering.docx')
doc.update_list_labels()
paras = doc.get_child_nodes(aw.NodeType.PARAGRAPH, True)
# Hitta om vi har styckelistan. I vårt dokument använder vår lista enkla arabiska siffror,
# som börjar på tre och slutar på sex.
for paragraph in list(filter(lambda p: p.list_format.is_list_item, list(filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_paragraph(), b), list(paras)))))):
    print(f'List item paragraph #{paras.index_of(paragraph)}')
    # Det här är texten vi får när vi skriver ut den här noden till textformat.
    # Denna textutmatning kommer att utelämna listetiketter. Ta bort eventuella styckeformateringstecken.
    paragraph_text = paragraph.to_string(save_format=aw.SaveFormat.TEXT).strip()
    print(f'\tExported Text: {paragraph_text}')
    label = paragraph.list_label
    # Detta hämtar positionen för stycket i den aktuella nivån i listan. Om vi har en lista med flera nivåer,
    # kommer detta att berätta vilken position den har på den nivån.
    print(f'\tNumerical Id: {label.label_value}')
    # Kombinera dem tillsammans för att inkludera listetiketten med texten i utmatningen.
    print(f'\tList label combined with text: {label.label_string} {paragraph_text}')
```

### See Also

* module [aspose.words](../../)
* class [Paragraph](../)

