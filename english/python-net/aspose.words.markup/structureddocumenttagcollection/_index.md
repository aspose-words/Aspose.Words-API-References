---
title: StructuredDocumentTagCollection class
linktitle: StructuredDocumentTagCollection class
articleTitle: StructuredDocumentTagCollection class
second_title: Aspose.Words for Python
description: "aspose.words.markup.StructuredDocumentTagCollection class. A collection of [IStructuredDocumentTag](../istructureddocumenttag/) instances that represent the structured document tags in the specified range"
type: docs
weight: 180
url: /python-net/aspose.words.markup/structureddocumenttagcollection/
---

## StructuredDocumentTagCollection class

A collection of [IStructuredDocumentTag](../istructureddocumenttag/) instances that represent the structured document tags in the specified range.
To learn more, visit the [Structured Document Tags or Content Control](https://docs.aspose.com/words/python-net/working-with-content-control-sdt/) documentation article.




### Indexers

| Name | Description |
| --- | --- |
| [``__getitem__(index)``](./__getitem__/#int) | Returns the structured document tag at the specified index. |

### Properties

| Name | Description |
| --- | --- |
| [count](./count/) | Returns the number of structured document tags in the collection. |

### Methods

| Name | Description |
| --- | --- |
|[ get_by_id(id)](./get_by_id/#int) | Returns the structured document tag by identifier. |
|[ get_by_tag(tag)](./get_by_tag/#str) | Returns the first structured document tag encountered in the collection with the specified tag. |
|[ get_by_title(title)](./get_by_title/#str) | Returns the first structured document tag encountered in the collection with the specified title. |
|[ remove(id)](./remove/#int) | Removes the structured document tag with the specified identifier. |
|[ remove_at(index)](./remove_at/#int) | Removes a structured document tag at the specified index. |

### Examples

Shows how to get structured document tag.

```python
doc = aw.Document(file_name=MY_DIR + 'Structured document tags by id.docx')
# Get the structured document tag by Id.
sdt = doc.range.structured_document_tags.get_by_id(1160505028)
print(sdt.is_multi_section)
print(sdt.title)
# Get the structured document tag or ranged tag by Title.
sdt = doc.range.structured_document_tags.get_by_title('Alias4')
print(sdt.id)
```

### See Also

* module [aspose.words.markup](../)

