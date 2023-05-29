---
title: SmartTag.accept method
linktitle: accept method
articleTitle: accept method
second_title: Aspose.Words for Python
description: "SmartTag.accept method. Accepts a visitor."
type: docs
weight: 60
url: /python-net/aspose.words.markup/smarttag/accept/
---

## accept(visitor) {#documentvisitor}

Accepts a visitor.


```python
def accept(self, visitor: aspose.words.DocumentVisitor):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| visitor | [DocumentVisitor](../../../aspose.words/documentvisitor/) |  |

Enumerates over this node and all of its children. Each node calls a corresponding method on [DocumentVisitor](../../../aspose.words/documentvisitor/).

For more info see the Visitor design pattern.




Calls [DocumentVisitor.visit_smart_tag_start()](../../../aspose.words/documentvisitor/visit_smart_tag_start/#smarttag), then calls [Node.accept()](../../../aspose.words/node/accept/#documentvisitor) for all
child nodes of the smart tag and calls [DocumentVisitor.visit_smart_tag_end()](../../../aspose.words/documentvisitor/visit_smart_tag_end/#smarttag) at the end.



### Returns

True if all nodes were visited; false if [DocumentVisitor](../../../aspose.words/documentvisitor/) stopped the operation before visiting all nodes.


### Examples

Shows how to create smart tags.

```python
def test_create(self):

    doc = aw.Document()

    # A smart tag appears in a document with Microsoft Word recognizes a part of its text as some form of data,
    # such as a name, date, or address, and converts it to a hyperlink that displays a purple dotted underline.
    smart_tag = aw.markup.SmartTag(doc)

    # Smart tags are composite nodes that contain their recognized text in its entirety.
    # Add contents to this smart tag manually.
    smart_tag.append_child(aw.Run(doc, "May 29, 2019"))

    # Microsoft Word may recognize the above contents as being a date.
    # Smart tags use the "Element" property to reflect the type of data they contain.
    smart_tag.element = "date"

    # Some smart tag types process their contents further into custom XML properties.
    smart_tag.properties.add(aw.markup.CustomXmlProperty("Day", "", "29"))
    smart_tag.properties.add(aw.markup.CustomXmlProperty("Month", "", "5"))
    smart_tag.properties.add(aw.markup.CustomXmlProperty("Year", "", "2019"))

    # Set the smart tag's URI to the default value.
    smart_tag.uri = "urn:schemas-microsoft-com:office:smarttags"

    doc.first_section.body.first_paragraph.append_child(smart_tag)
    doc.first_section.body.first_paragraph.append_child(aw.Run(doc, " is a date. "))

    # Create another smart tag for a stock ticker.
    smart_tag = aw.markup.SmartTag(doc)
    smart_tag.element = "stockticker"
    smart_tag.uri = "urn:schemas-microsoft-com:office:smarttags"

    smart_tag.append_child(aw.Run(doc, "MSFT"))

    doc.first_section.body.first_paragraph.append_child(smart_tag)
    doc.first_section.body.first_paragraph.append_child(aw.Run(doc, " is a stock ticker."))

    # Print all the smart tags in our document using a document visitor.
    #doc.accept(ExSmartTag.SmartTagPrinter())

    # Older versions of Microsoft Word support smart tags.
    doc.save(ARTIFACTS_DIR + "SmartTag.create.doc")

    # Use the "remove_smart_tags" method to remove all smart tags from a document.
    self.assertEqual(2, doc.get_child_nodes(aw.NodeType.SMART_TAG, True).count)

    doc.remove_smart_tags()

    self.assertEqual(0, doc.get_child_nodes(aw.NodeType.SMART_TAG, True).count)

#class SmartTagPrinter(aw.DocumentVisitor):
#    """Prints visited smart tags and their contents."""

#    def visit_smart_tag_start(smart_tag: aw.markup.SmartTag) -> aw.VisitorAction:
#        """Called when a SmartTag node is encountered in the document."""

#        print(f"Smart tag type: {smart_tag.element}")
#        return aw.VisitorAction.CONTINUE

#    def visit_smart_tag_end(smart_tag: aw.markup.SmartTag) -> aw.VisitorAction:
#        """Called when the visiting of a SmartTag node is ended."""

#        print(f"\tContents: \"{smart_tag.to_string(aw.SaveFormat.TEXT)}\"")

#        if smart_tag.properties.count == 0:
#            print("\tContains no properties")
#        else:

#            print("\tProperties: ", end="")
#            properties = string[smart_tag.properties.count]
#            index = 0

#            for cxp in smart_tag.properties:
#                properties[index] = f'"{cxp.Name}" = "{cxp.Value}"'
#                index += 1

#            print("".join(", ", properties))

#        return aw.VisitorAction.CONTINUE
```

### See Also

* module [aspose.words.markup](../../)
* class [SmartTag](../)

