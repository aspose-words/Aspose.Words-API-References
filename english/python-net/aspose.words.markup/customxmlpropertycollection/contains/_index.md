---
title: CustomXmlPropertyCollection.contains method
linktitle: contains method
articleTitle: contains method
second_title: Aspose.Words for Python
description: "CustomXmlPropertyCollection.contains method. Determines whether the collection contains a property with the given name."
type: docs
weight: 50
url: /python-net/aspose.words.markup/customxmlpropertycollection/contains/
---

## contains(name) {#str}

Determines whether the collection contains a property with the given name.


```python
def contains(self, name: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| name | str | Case-sensitive name of the property to locate. |

### Returns

``True`` if the item is found in the collection; otherwise, ``False``.


### Examples

Shows how to work with smart tag properties to get in depth information about smart tags.

```python
doc = aw.Document(MY_DIR + "Smart tags.doc")

# A smart tag appears in a document with Microsoft Word recognizes a part of its text as some form of data,
# such as a name, date, or address, and converts it to a hyperlink that displays a purple dotted underline.
# In Word 2003, we can enable smart tags via "Tools" -> "AutoCorrect options..." -> "SmartTags".
# In our input document, there are three objects that Microsoft Word registered as smart tags.
# Smart tags may be nested, so this collection contains more.
smart_tags = [node.as_smart_tag() for node in doc.get_child_nodes(aw.NodeType.SMART_TAG, True)]

self.assertEqual(8, len(smart_tags))

# The "properties" member of a smart tag contains its metadata, which will be different for each type of smart tag.
# The properties of a "date"-type smart tag contain its year, month, and day.
properties = smart_tags[7].properties

self.assertEqual(4, properties.count)

for prop in properties:
    print(f"Property name: {prop.name}, value: {prop.value}")
    self.assertEqual("", prop.uri)

# We can also access the properties in various ways, such as a key-value pair.
self.assertTrue(properties.contains("Day"))
self.assertEqual("22", properties.get_by_name("Day").value)
self.assertEqual("2003", properties[2].value)
self.assertEqual(1, properties.index_of_key("Month"))

# Below are three ways of removing elements from the properties collection.
# 1 -  Remove by index:
properties.remove_at(3)

self.assertEqual(3, properties.count)

# 2 -  Remove by name:
properties.remove("Year")

self.assertEqual(2, properties.count)

# 3 -  Clear the entire collection at once:
properties.clear()

self.assertEqual(0, properties.count)
```

### See Also

* module [aspose.words.markup](../../)
* class [CustomXmlPropertyCollection](../)

