---
title: Paragraph.list_label property
linktitle: list_label property
articleTitle: list_label property
second_title: Aspose.Words for Python
description: "Paragraph.list_label property. Gets a [Paragraph.list_label](./) object that provides access to list numbering value and formatting for this paragraph."
type: docs
weight: 160
url: /fr/python-net/aspose.words/paragraph/list_label/
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
# Trouver si nous avons la liste de paragraphes. Dans notre document, notre liste utilise des nombres arabes simples,
# qui commence à trois et se termine à six.
for paragraph in list(filter(lambda p: p.list_format.is_list_item, list(filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_paragraph(), b), list(paras)))))):
    print(f'List item paragraph #{paras.index_of(paragraph)}')
    # Ceci est le texte que nous obtenons lorsque nous exportons ce nœud au format texte.
    # Cette sortie texte omettra les étiquettes de liste. Supprimez tout caractère de formatage de paragraphe.
    paragraph_text = paragraph.to_string(save_format=aw.SaveFormat.TEXT).strip()
    print(f'\tExported Text: {paragraph_text}')
    label = paragraph.list_label
    # Cela récupère la position du paragraphe dans le niveau actuel de la liste. Si nous avons une liste à plusieurs niveaux,
    # cela nous indiquera quelle position il occupe à ce niveau.
    print(f'\tNumerical Id: {label.label_value}')
    # Combinez-les pour inclure l'étiquette de liste avec le texte dans la sortie.
    print(f'\tList label combined with text: {label.label_string} {paragraph_text}')
```

### See Also

* module [aspose.words](../../)
* class [Paragraph](../)

