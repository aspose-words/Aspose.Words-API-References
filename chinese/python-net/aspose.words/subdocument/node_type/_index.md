---
title: SubDocument.node_type property
linktitle: node_type property
articleTitle: node_type property
second_title: Aspose.Words for Python
description: "SubDocument.node_type property. Returns [NodeType.SUB_DOCUMENT](../../nodetype/#SUB_DOCUMENT)."
type: docs
weight: 10
url: /zh/python-net/aspose.words/subdocument/node_type/
---

## SubDocument.node_type property

Returns [NodeType.SUB_DOCUMENT](../../nodetype/#SUB_DOCUMENT).



```python
@property
def node_type(self) -> aspose.words.NodeType:
    ...

```

### Examples

Shows how to access a master document's subdocument.

```python
doc = aw.Document(file_name=MY_DIR + 'Master document.docx')
sub_documents = doc.get_child_nodes(aw.NodeType.SUB_DOCUMENT, True)
# 此节点用作对外部文档的引用，且其内容无法访问。
sub_document = sub_documents[0].as_sub_document()
self.assertFalse(sub_document.is_composite)
```

### See Also

* module [aspose.words](../../)
* class [SubDocument](../)

