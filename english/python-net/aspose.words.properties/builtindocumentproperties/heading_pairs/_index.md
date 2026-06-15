---
title: BuiltInDocumentProperties.heading_pairs property
linktitle: heading_pairs property
articleTitle: heading_pairs property
second_title: Aspose.Words for Python
description: "BuiltInDocumentProperties.heading_pairs property. Specifies document headings and their names."
type: docs
weight: 120
url: /python-net/aspose.words.properties/builtindocumentproperties/heading_pairs/
---

## BuiltInDocumentProperties.heading_pairs property

Specifies document headings and their names.


```python
@property
def heading_pairs(self) -> List[object]:
    ...

@heading_pairs.setter
def heading_pairs(self, value: List[object]):
    ...

```

### Remarks

Every heading pair occupies two elements in this array.

The first element of the pair is a string and specifies the heading name.
The second element of the pair is an int and specifies the count of document
parts for this heading in the [BuiltInDocumentProperties.titles_of_parts](../titles_of_parts/) property.

The total sum of counts for all heading pairs in this property must be equal to the
number of elements in the [BuiltInDocumentProperties.titles_of_parts](../titles_of_parts/) property.

Aspose.Words does not update this property.




### See Also

* module [aspose.words.properties](../../)
* class [BuiltInDocumentProperties](../)
* property [BuiltInDocumentProperties.titles_of_parts](../titles_of_parts/)

