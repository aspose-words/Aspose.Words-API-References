---
title: AdvancedCompareOptions.compare_list_definitions property
linktitle: compare_list_definitions property
articleTitle: compare_list_definitions property
second_title: Aspose.Words for Python
description: "AdvancedCompareOptions.compare_list_definitions property. Specifies whether list definition contents are compared instead of list definition Ids."
type: docs
weight: 20
url: /python-net/aspose.words.comparing/advancedcompareoptions/compare_list_definitions/
---

## AdvancedCompareOptions.compare_list_definitions property

Specifies whether list definition contents are compared instead of list definition Ids.


```python
@property
def compare_list_definitions(self) -> bool:
    ...

@compare_list_definitions.setter
def compare_list_definitions(self, value: bool):
    ...

```

### Remarks

Default value is ``False``.



### Examples

Shows how to control whether list definition content will be compared during document comparison.

```python
doc_a = aw.Document()
builder_a = aw.DocumentBuilder(doc=doc_a)
builder_a.list_format.apply_number_default()
builder_a.writeln("Item 1")
builder_a.writeln("Item 2")
builder_a.list_format.remove_numbers()
doc_b = aw.Document()
builder_b = aw.DocumentBuilder(doc=doc_b)
builder_b.list_format.apply_bullet_default()
builder_b.writeln("Item 1")
builder_b.writeln("Item 2")
builder_b.list_format.remove_numbers()
# Compare documents with CompareListDefinitions enabled.

options = aw.comparing.CompareOptions() 
options.advanced_options.compare_list_definitions = is_compare_list_definitions

doc_a.compare(document=doc_b, author="test", date_time=datetime.datetime.now(), options=options)
```

### See Also

* module [aspose.words.comparing](../../)
* class [AdvancedCompareOptions](../)

