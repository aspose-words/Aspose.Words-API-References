---
title: AdvancedCompareOptions.ignore_dml_unique_id property
linktitle: ignore_dml_unique_id property
articleTitle: ignore_dml_unique_id property
second_title: Aspose.Words for Python
description: "AdvancedCompareOptions.ignore_dml_unique_id property. Specifies whether to ignore difference in DrawingML unique Id."
type: docs
weight: 30
url: /fr/python-net/aspose.words.comparing/advancedcompareoptions/ignore_dml_unique_id/
---

## AdvancedCompareOptions.ignore_dml_unique_id property

Specifies whether to ignore difference in DrawingML unique Id.


```python
@property
def ignore_dml_unique_id(self) -> bool:
    ...

@ignore_dml_unique_id.setter
def ignore_dml_unique_id(self, value: bool):
    ...

```

### Remarks

Default value is ``False``.



### Examples

Shows how to compare documents ignoring DML unique ID.

```python
doc_a = aw.Document(file_name=MY_DIR + 'DML unique ID original.docx')
doc_b = aw.Document(file_name=MY_DIR + 'DML unique ID compare.docx')
# Par défaut, Aspose.Words n'ignore pas l'ID unique du DML, et le nombre de révisions était de 2.
# Si nous ignorons l'ID unique du DML, et que le nombre de révisions était de 0.
compare_options = aw.comparing.CompareOptions()
compare_options.advanced_options.ignore_dml_unique_id = is_ignore_dml_unique_id
doc_a.compare(document=doc_b, author='Aspose.Words', date_time=datetime.datetime.now(), options=compare_options)
self.assertEqual(1 if is_ignore_dml_unique_id else 3, doc_a.revisions.count)
```

### See Also

* module [aspose.words.comparing](../../)
* class [AdvancedCompareOptions](../)

