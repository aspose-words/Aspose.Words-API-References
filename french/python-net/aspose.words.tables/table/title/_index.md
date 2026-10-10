---
title: Table.title property
linktitle: title property
articleTitle: title property
second_title: Aspose.Words for Python
description: "Table.title property. Gets or sets title of this table"
type: docs
weight: 320
url: /fr/python-net/aspose.words.tables/table/title/
---

## Table.title property

Gets or sets title of this table.
It provides an alternative text representation of the information contained in the table.


```python
@property
def title(self) -> str:
    ...

@title.setter
def title(self, value: str):
    ...

```

### Remarks

The default value is an empty string.

This property is meaningful for ISO/IEC 29500 compliant DOCX documents
([OoxmlCompliance](../../../aspose.words.saving/ooxmlcompliance/)).
When saved to pre-ISO/IEC 29500 formats, the property is ignored.




### Examples

Shows how to build a nested table without using a document builder.

```python
doc = aw.Document()
# Créez le tableau extérieur avec trois lignes et quatre colonnes, puis ajoutez-le au document.
outer_table = ExTable._create_table(doc, 3, 4, 'Outer Table')
doc.first_section.body.append_child(outer_table)
# Créez un autre tableau avec deux lignes et deux colonnes, puis insérez-le dans la première cellule du premier tableau.
inner_table = ExTable._create_table(doc, 2, 2, 'Inner Table')
outer_table.first_row.first_cell.append_child(inner_table)
doc.save(file_name=ARTIFACTS_DIR + 'Table.CreateNestedTable.docx')
```

Shows how to build a nested table without using a document builder (CreateTable).

```python
@staticmethod
def _create_table(doc, row_count, cell_count, cell_text):
    table = aw.tables.Table(doc)
    row_id = 1
    while row_id <= row_count:
        row = aw.tables.Row(doc)
        table.append_child(row)
        cell_id = 1
        while cell_id <= cell_count:
            cell = aw.tables.Cell(doc)
            cell.append_child(aw.Paragraph(doc))
            cell.first_paragraph.append_child(aw.Run(doc=doc, text=cell_text))
            row.append_child(cell)
            cell_id += 1
        row_id += 1
    # Vous pouvez utiliser les propriétés "Title" et "Description" pour ajouter respectivement un titre et une description à votre tableau.
    # Le tableau doit contenir au moins une ligne avant que nous puissions utiliser ces propriétés.
    # Ces propriétés sont pertinentes pour les documents .docx conformes à la norme ISO / IEC 29500 (voir la classe OoxmlCompliance).
    # Si nous enregistrons le document dans des formats antérieurs à ISO/IEC 29500, Microsoft Word ignore ces propriétés.
    table.title = 'Aspose table title'
    table.description = 'Aspose table description'
    return table
```

### See Also

* module [aspose.words.tables](../../)
* class [Table](../)

