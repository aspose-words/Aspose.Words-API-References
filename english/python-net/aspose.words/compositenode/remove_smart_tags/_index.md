---
title: CompositeNode.remove_smart_tags method
linktitle: remove_smart_tags method
articleTitle: remove_smart_tags method
second_title: Aspose.Words for Python
description: "CompositeNode.remove_smart_tags method. Removes all [SmartTag](../../../aspose.words.markup/smarttag/) descendant nodes of the current node."
type: docs
weight: 180
url: /python-net/aspose.words/compositenode/remove_smart_tags/
---

## remove_smart_tags() {#default}

Removes all [SmartTag](../../../aspose.words.markup/smarttag/) descendant nodes of the current node.



```python
def remove_smart_tags(self):
    ...
```

### Remarks

This method does not remove the content of the smart tags.


### Examples

Removes all smart tags from descendant nodes of a composite node.

```python
doc = aw.Document(file_name=MY_DIR + 'Smart tags.doc')
self.assertEqual(8, doc.get_child_nodes(aw.NodeType.SMART_TAG, True).count)
doc.remove_smart_tags()
self.assertEqual(0, doc.get_child_nodes(aw.NodeType.SMART_TAG, True).count)
```

### See Also

* module [aspose.words](../../)
* class [CompositeNode](../)

