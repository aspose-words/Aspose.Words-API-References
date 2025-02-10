---
title: FieldEQ.as_office_math method
linktitle: as_office_math method
articleTitle: as_office_math method
second_title: Aspose.Words for Python
description: "FieldEQ.as_office_math method. Returns Office Math object corresponded to the EQ field."
type: docs
weight: 20
url: /python-net/aspose.words.fields/fieldeq/as_office_math/
---

## as_office_math() {#default}

Returns Office Math object corresponded to the EQ field.


```python
def as_office_math(self):
    ...
```

### Returns

Returns ``None`` if field code is empty or invalid, otherwise an [OfficeMath](../../../aspose.words.math/officemath/) instance.



### Examples

Shows how to replace the EQ field with Office Math.

```python
doc = aw.Document(file_name=MY_DIR + 'Field sample - EQ.docx')
field_eq = list(filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_field_eq(), b), list(doc.range.fields))))[0]
office_math = field_eq.as_office_math()
field_eq.start.parent_node.insert_before(office_math, field_eq.start)
field_eq.remove()
doc.save(file_name=ARTIFACTS_DIR + 'Field.EQAsOfficeMath.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldEQ](../)

