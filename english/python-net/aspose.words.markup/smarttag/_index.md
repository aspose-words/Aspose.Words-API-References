﻿---
title: SmartTag class
linktitle: SmartTag class
articleTitle: SmartTag class
second_title: Aspose.Words for Python
description: "aspose.words.markup.SmartTag class. This element specifies the presence of a smart tag around one or more inline structures (runs, images, fields,etc.) within a paragraph"
type: docs
weight: 160
url: /python-net/aspose.words.markup/smarttag/
---

## SmartTag class

This element specifies the presence of a smart tag around one or more inline structures
(runs, images, fields,etc.) within a paragraph.
To learn more, visit the [Structured Document Tags or Content Control](https://docs.aspose.com/words/python-net/working-with-content-control-sdt/) documentation article.




Smart tags is a kind of custom XML markup. Smart tags provide a facility for embedding
customer-defined semantics into the document via the ability to provide a basic namespace/name
for a run or set of runs within a document.

[SmartTag](./) can be a child of a [Paragraph](../../aspose.words/paragraph/) or
another [SmartTag](./) node.

The complete list of child nodes that can occur inside a smart tag consists of
[BookmarkStart](../../aspose.words/bookmarkstart/), [BookmarkEnd](../../aspose.words/bookmarkend/),
[FieldStart](../../aspose.words.fields/fieldstart/), [FieldSeparator](../../aspose.words.fields/fieldseparator/), [FieldEnd](../../aspose.words.fields/fieldend/), [FormField](../../aspose.words.fields/formfield/),
[Comment](../../aspose.words/comment/), [Footnote](../../aspose.words.notes/footnote/),
[Run](../../aspose.words/run/), [SpecialChar](../../aspose.words/specialchar/),
[Shape](../../aspose.words.drawing/shape/), [GroupShape](../../aspose.words.drawing/groupshape/),
[CommentRangeStart](../../aspose.words/commentrangestart/),
[CommentRangeEnd](../../aspose.words/commentrangeend/),
[SmartTag](./).




**Inheritance:** [SmartTag](./) → [CompositeNode](../../aspose.words/compositenode/) → [Node](../../aspose.words/node/)

### Constructors
| Name | Description |
| --- | --- |
| [SmartTag(doc)](./__init__/#documentbase) | Initializes a new instance of the [SmartTag](./) class. |

### Properties

| Name | Description |
| --- | --- |
| [count](../../aspose.words/compositenode/count/) | Gets the number of immediate children of this node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
| [custom_node_id](../../aspose.words/node/custom_node_id/) | Specifies custom node identifier.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [document](../../aspose.words/node/document/) | Gets the document to which this node belongs.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [element](./element/) | Specifies the name of the smart tag within the document. |
| [first_child](../../aspose.words/compositenode/first_child/) | Gets the first child of the node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
| [has_child_nodes](../../aspose.words/compositenode/has_child_nodes/) | Returns ``True`` if this node has any child nodes.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
| [is_composite](../../aspose.words/node/is_composite/) | Returns ``True`` if this node can contain other nodes.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [last_child](../../aspose.words/compositenode/last_child/) | Gets the last child of the node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
| [next_sibling](../../aspose.words/node/next_sibling/) | Gets the node immediately following this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [node_type](./node_type/) | Returns [NodeType.SMART_TAG](../../aspose.words/nodetype/#SMART_TAG). |
| [parent_node](../../aspose.words/node/parent_node/) | Gets the immediate parent of this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [previous_sibling](../../aspose.words/node/previous_sibling/) | Gets the node immediately preceding this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [properties](./properties/) | A collection of the smart tag properties. |
| [range](../../aspose.words/node/range/) | Returns a [Range](../../aspose.words/range/) object that represents the portion of a document that is contained in this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [uri](./uri/) | Specifies the namespace URI of the smart tag. |

### Methods

| Name | Description |
| --- | --- |
|[ accept(visitor)](./accept/#documentvisitor) | Accepts a visitor. |
|[ append_child(new_child)](../../aspose.words/compositenode/append_child/#node) | Adds the specified node to the end of the list of child nodes for this node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ clone(is_clone_children)](../../aspose.words/node/clone/#bool) | Creates a duplicate of the node.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ get_ancestor(ancestor_type)](../../aspose.words/node/get_ancestor/#unknown) | Gets the first ancestor of the specified object type.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ get_ancestor(ancestor_type)](../../aspose.words/node/get_ancestor/#nodetype) | Gets the first ancestor of the specified [NodeType](../../aspose.words/nodetype/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ get_child(node_type, index, is_deep)](../../aspose.words/compositenode/get_child/#nodetype_int_bool) | Returns an Nth child node that matches the specified type.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ get_child_nodes(node_type, is_deep)](../../aspose.words/compositenode/get_child_nodes/#nodetype_bool) | Returns a live collection of child nodes that match the specified type.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ get_text()](../../aspose.words/node/get_text/#default) | Gets the text of this node and of all its children.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ index_of(child)](../../aspose.words/compositenode/index_of/#node) | Returns the index of the specified child node in the child node array.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ insert_after(new_child, ref_child)](../../aspose.words/compositenode/insert_after/#node_node) | Inserts the specified node immediately after the specified reference node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ insert_before(new_child, ref_child)](../../aspose.words/compositenode/insert_before/#node_node) | Inserts the specified node immediately before the specified reference node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ next_pre_order(root_node)](../../aspose.words/node/next_pre_order/#node) | Gets next node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ node_type_to_string(node_type)](../../aspose.words/node/node_type_to_string/#nodetype) | A utility method that converts a node type enum value into a user friendly string.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ prepend_child(new_child)](../../aspose.words/compositenode/prepend_child/#node) | Adds the specified node to the beginning of the list of child nodes for this node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ previous_pre_order(root_node)](../../aspose.words/node/previous_pre_order/#node) | Gets the previous node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ remove()](../../aspose.words/node/remove/#default) | Removes itself from the parent.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ remove_all_children()](../../aspose.words/compositenode/remove_all_children/#default) | Removes all the child nodes of the current node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ remove_child(old_child)](../../aspose.words/compositenode/remove_child/#node) | Removes the specified child node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ remove_smart_tags()](../../aspose.words/compositenode/remove_smart_tags/#default) | Removes all [SmartTag](./) descendant nodes of the current node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ select_nodes(xpath)](../../aspose.words/compositenode/select_nodes/#str) | Selects a list of nodes matching the XPath expression.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ select_single_node(xpath)](../../aspose.words/compositenode/select_single_node/#str) | Selects the first [Node](../../aspose.words/node/) that matches the XPath expression.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ to_string(save_format)](../../aspose.words/node/to_string/#saveformat) | Exports the content of the node into a string in the specified format.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ to_string(save_options)](../../aspose.words/node/to_string/#saveoptions) | Exports the content of the node into a string using the specified save options.<br>(Inherited from [Node](../../aspose.words/node/)) |

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

* module [aspose.words.markup](../)
* class [CompositeNode](../../aspose.words/compositenode/)

