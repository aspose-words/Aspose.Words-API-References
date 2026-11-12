---
title: CompareOptions.ignore_dml_unique_id property
linktitle: ignore_dml_unique_id property
articleTitle: ignore_dml_unique_id property
second_title: Aspose.Words for Python
description: "CompareOptions.ignore_dml_unique_id property. Specifies whether to ignore difference in DrawingML unique Id."
type: docs
weight: 70
url: /ru/python-net/aspose.words.comparing/compareoptions/ignore_dml_unique_id/
---

## CompareOptions.ignore_dml_unique_id property

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
# По умолчанию Aspose.Words не игнорирует уникальный идентификатор DML, и количество правок было 2.
# Если мы игнорируем уникальный идентификатор DML, и количество правок равно 0.
compare_options = aw.comparing.CompareOptions()
compare_options.advanced_options.ignore_dml_unique_id = is_ignore_dml_unique_id
doc_a.compare(document=doc_b, author='Aspose.Words', date_time=datetime.datetime.now(), options=compare_options)
self.assertEqual(1 if is_ignore_dml_unique_id else 3, doc_a.revisions.count)
```

### See Also

* module [aspose.words.comparing](../../)
* class [CompareOptions](../)

