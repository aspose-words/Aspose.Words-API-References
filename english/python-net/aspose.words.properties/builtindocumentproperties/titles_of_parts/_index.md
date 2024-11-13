---
title: BuiltInDocumentProperties.titles_of_parts property
linktitle: titles_of_parts property
articleTitle: titles_of_parts property
second_title: Aspose.Words for Python
description: "BuiltInDocumentProperties.titles_of_parts property. Each string in the array specifies the name of a part in the document."
type: docs
weight: 330
url: /python-net/aspose.words.properties/builtindocumentproperties/titles_of_parts/
---

## BuiltInDocumentProperties.titles_of_parts property

Each string in the array specifies the name of a part in the document.


```python
@property
def titles_of_parts(self) -> List[str]:
    ...

@titles_of_parts.setter
def titles_of_parts(self, value: List[str]):
    ...

```

### Remarks

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
* property [BuiltInDocumentProperties.heading_pairs](../heading_pairs/)

