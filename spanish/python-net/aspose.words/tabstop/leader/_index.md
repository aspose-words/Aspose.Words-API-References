---
title: TabStop.leader property
linktitle: leader property
articleTitle: leader property
second_title: Aspose.Words for Python
description: "TabStop.leader property. Gets or sets the type of the leader line displayed under the tab character."
type: docs
weight: 40
url: /es/python-net/aspose.words/tabstop/leader/
---

## TabStop.leader property

Gets or sets the type of the leader line displayed under the tab character.


```python
@property
def leader(self) -> aspose.words.TabLeader:
    ...

@leader.setter
def leader(self, value: aspose.words.TabLeader):
    ...

```

### Examples

Shows how to modify the position of the right tab stop in TOC related paragraphs.

```python
doc = aw.Document(file_name=MY_DIR + 'Table of contents.docx')
# Iterar a través de todos los párrafos con estilos basados en resultados de TOC; esto es cualquier estilo entre TOC y TOC9.
for para in doc.get_child_nodes(aw.NodeType.PARAGRAPH, True):
    para = para.as_paragraph()
    if para.paragraph_format.style.style_identifier >= aw.StyleIdentifier.TOC1 and para.paragraph_format.style.style_identifier <= aw.StyleIdentifier.TOC9:
        # Obtener la primera tabulación usada en este párrafo, debería ser la tabulación utilizada para alinear los números de página.
        tab = para.paragraph_format.tab_stops[0]
        # Reemplazar la primera tabulación predeterminada, detenerse con una tabulación personalizada.
        para.paragraph_format.tab_stops.remove_by_position(tab.position)
        para.paragraph_format.tab_stops.add(position=tab.position - 50, alignment=tab.alignment, leader=tab.leader)
doc.save(file_name=ARTIFACTS_DIR + 'Styles.ChangeTocsTabStops.docx')
```

### See Also

* module [aspose.words](../../)
* class [TabStop](../)

