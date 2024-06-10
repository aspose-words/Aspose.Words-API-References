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




### Examples

Shows the relationship between "heading_pairs" and "titles_of_parts" properties.

```python
doc = aw.Document(MY_DIR + 'Heading pairs and titles of parts.docx')
# We can find the combined values of these collections via
# "File" -> "Properties" -> "Advanced Properties" -> "Contents" tab.
# The "heading_pairs" property is a collection of [string, int] pairs that
# determines how many document parts a heading spans across.
heading_pairs = doc.built_in_document_properties.heading_pairs
# The "titles_of_parts" property contains the names of parts that belong to the above headings.
titles_of_parts = doc.built_in_document_properties.titles_of_parts
heading_pairs_index = 0
titles_of_parts_index = 0
while heading_pairs_index < len(heading_pairs):
    print(f'Parts for {heading_pairs[heading_pairs_index]}:')
    heading_pairs_index += 1
    parts_count = int(heading_pairs[heading_pairs_index])
    heading_pairs_index += 1
    for i in range(parts_count):
        print(f'\t"{titles_of_parts[titles_of_parts_index]}"')
        titles_of_parts_index += 1
```

### See Also

* module [aspose.words.properties](../../)
* class [BuiltInDocumentProperties](../)
* property [BuiltInDocumentProperties.titles_of_parts](../titles_of_parts/)

