﻿---
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

Shows how to create smart tags.

```python
def create():
    doc = aw.Document()
    # A smart tag appears in a document with Microsoft Word recognizes a part of its text as some form of data,
    # such as a name, date, or address, and converts it to a hyperlink that displays a purple dotted underline.
    smart_tag = aw.markup.SmartTag(doc)
    # Smart tags are composite nodes that contain their recognized text in its entirety.
    # Add contents to this smart tag manually.
    smart_tag.append_child(aw.Run(doc, 'May 29, 2019'))
    # Microsoft Word may recognize the above contents as being a date.
    # Smart tags use the "Element" property to reflect the type of data they contain.
    smart_tag.element = 'date'
    # Some smart tag types process their contents further into custom XML properties.
    smart_tag.properties.add(aw.markup.CustomXmlProperty('Day', '', '29'))
    smart_tag.properties.add(aw.markup.CustomXmlProperty('Month', '', '5'))
    smart_tag.properties.add(aw.markup.CustomXmlProperty('Year', '', '2019'))
    # Set the smart tag's URI to the default value.
    smart_tag.uri = 'urn:schemas-microsoft-com:office:smarttags'
    doc.first_section.body.first_paragraph.append_child(smart_tag)
    doc.first_section.body.first_paragraph.append_child(aw.Run(doc, ' is a date. '))
    # Create another smart tag for a stock ticker.
    smart_tag = aw.markup.SmartTag(doc)
    smart_tag.element = 'stockticker'
    smart_tag.uri = 'urn:schemas-microsoft-com:office:smarttags'
    smart_tag.append_child(aw.Run(doc, 'MSFT'))
    doc.first_section.body.first_paragraph.append_child(smart_tag)
    doc.first_section.body.first_paragraph.append_child(aw.Run(doc, ' is a stock ticker.'))
    # Older versions of Microsoft Word support smart tags.
    doc.save(ARTIFACTS_DIR + 'SmartTag.create.doc')
    # Use the "remove_smart_tags" method to remove all smart tags from a document.
    self.assertEqual(2, doc.get_child_nodes(aw.NodeType.SMART_TAG, True).count)
    doc.remove_smart_tags()
    self.assertEqual(0, doc.get_child_nodes(aw.NodeType.SMART_TAG, True).count)
```

### See Also

* module [aspose.words](../../)
* class [CompositeNode](../)

