---
title: FieldToc.captionless_table_of_figures_label property
linktitle: captionless_table_of_figures_label property
articleTitle: captionless_table_of_figures_label property
second_title: Aspose.Words for Python
description: "FieldToc.captionless_table_of_figures_label property. Gets or sets the name of the sequence identifier used when building a table of figures that does not include caption's label and number."
type: docs
weight: 30
url: /python-net/aspose.words.fields/fieldtoc/captionless_table_of_figures_label/
---

## FieldToc.captionless_table_of_figures_label property

Gets or sets the name of the sequence identifier used when building a table of figures that does not include caption's
label and number.


```python
@property
def captionless_table_of_figures_label(self) -> str:
    ...

@captionless_table_of_figures_label.setter
def captionless_table_of_figures_label(self, value: str):
    ...

```

### Examples

Shows how to set the name of the sequence identifier.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
field_toc = builder.insert_field(field_type=aw.fields.FieldType.FIELD_TOC, update_field=True).as_field_toc()
field_toc.captionless_table_of_figures_label = 'Test'
self.assertEqual(' TOC  \\a Test', field_toc.get_field_code())
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldToc](../)

