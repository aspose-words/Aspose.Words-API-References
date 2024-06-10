---
title: HeaderFooter class
linktitle: HeaderFooter class
articleTitle: HeaderFooter class
second_title: Aspose.Words for Python
description: "aspose.words.HeaderFooter class. Represents a container for the header or footer text of a section"
type: docs
weight: 440
url: /python-net/aspose.words/headerfooter/
---

## HeaderFooter class

Represents a container for the header or footer text of a section.
To learn more, visit the [Working with Headers and Footers](https://docs.aspose.com/words/python-net/working-with-headers-and-footers/) documentation article.




### Remarks

[HeaderFooter](./) can contain [Paragraph](../paragraph/) and [Table](../../aspose.words.tables/table/) child nodes.

[HeaderFooter](./) is a section-level node and can only be a child of [Section](../section/).
There can only be one [HeaderFooter](./) of each [HeaderFooter.header_footer_type](./header_footer_type/) in a [Section](../section/).

If [Section](../section/) does not have a [HeaderFooter](./) of a specific type or
the [HeaderFooter](./) has no child nodes, this header/footer is considered linked to
the header/footer of the same type of the previous section in Microsoft Word.

When [HeaderFooter](./) contains at least one [Paragraph](../paragraph/), it is no longer
considered linked to previous in Microsoft Word.




**Inheritance:** [HeaderFooter](./) → [Story](../story/) → [CompositeNode](../compositenode/) → [Node](../node/)

### Constructors
| Name | Description |
| --- | --- |
| [HeaderFooter(doc, header_footer_type)](./__init__/#documentbase_headerfootertype) | Creates a new header or footer of the specified type. |

### Properties

| Name | Description |
| --- | --- |
| [count](../compositenode/count/) | Gets the number of immediate children of this node.<br>(Inherited from [CompositeNode](../compositenode/)) |
| [custom_node_id](../node/custom_node_id/) | Specifies custom node identifier.<br>(Inherited from [Node](../node/)) |
| [document](../node/document/) | Gets the document to which this node belongs.<br>(Inherited from [Node](../node/)) |
| [first_child](../compositenode/first_child/) | Gets the first child of the node.<br>(Inherited from [CompositeNode](../compositenode/)) |
| [first_paragraph](../story/first_paragraph/) | Gets the first paragraph in the story.<br>(Inherited from [Story](../story/)) |
| [has_child_nodes](../compositenode/has_child_nodes/) | Returns ``True`` if this node has any child nodes.<br>(Inherited from [CompositeNode](../compositenode/)) |
| [header_footer_type](./header_footer_type/) | Gets the type of this header/footer. |
| [is_composite](../node/is_composite/) | Returns ``True`` if this node can contain other nodes.<br>(Inherited from [Node](../node/)) |
| [is_header](./is_header/) | True if this [HeaderFooter](./) object is a header. |
| [is_linked_to_previous](./is_linked_to_previous/) | True if this header or footer is linked to the corresponding header or footer in the previous section. |
| [last_child](../compositenode/last_child/) | Gets the last child of the node.<br>(Inherited from [CompositeNode](../compositenode/)) |
| [last_paragraph](../story/last_paragraph/) | Gets the last paragraph in the story.<br>(Inherited from [Story](../story/)) |
| [next_sibling](../node/next_sibling/) | Gets the node immediately following this node.<br>(Inherited from [Node](../node/)) |
| [node_type](./node_type/) | Returns [NodeType.HEADER_FOOTER](../nodetype/#HEADER_FOOTER). |
| [paragraphs](../story/paragraphs/) | Gets a collection of paragraphs that are immediate children of the story.<br>(Inherited from [Story](../story/)) |
| [parent_node](../node/parent_node/) | Gets the immediate parent of this node.<br>(Inherited from [Node](../node/)) |
| [parent_section](./parent_section/) | Gets the parent section of this story. |
| [previous_sibling](../node/previous_sibling/) | Gets the node immediately preceding this node.<br>(Inherited from [Node](../node/)) |
| [range](../node/range/) | Returns a [Range](../range/) object that represents the portion of a document that is contained in this node.<br>(Inherited from [Node](../node/)) |
| [story_type](../story/story_type/) | Gets the type of this story.<br>(Inherited from [Story](../story/)) |
| [tables](../story/tables/) | Gets a collection of tables that are immediate children of the story.<br>(Inherited from [Story](../story/)) |

### Methods

| Name | Description |
| --- | --- |
|[ accept(visitor)](./accept/#documentvisitor) | Accepts a visitor. |
|[ accept_end(visitor)](./accept_end/#documentvisitor) | Accepts a visitor for visiting the end of the header. |
|[ accept_start(visitor)](./accept_start/#documentvisitor) | Accepts a visitor for visiting the start of the header. |
|[ append_child(new_child)](../compositenode/append_child/#node) | Adds the specified node to the end of the list of child nodes for this node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ append_paragraph(text)](../story/append_paragraph/#str) | A shortcut method that creates a [Paragraph](../paragraph/) object with optional text and appends it to the end of this object.<br>(Inherited from [Story](../story/)) |
|[ clone(is_clone_children)](../node/clone/#bool) | Creates a duplicate of the node.<br>(Inherited from [Node](../node/)) |
|[ delete_shapes()](../story/delete_shapes/#default) | Deletes all shapes from the text of this story.<br>(Inherited from [Story](../story/)) |
|[ get_ancestor(ancestor_type)](../node/get_ancestor/#object) | Gets the first ancestor of the specified object type.<br>(Inherited from [Node](../node/)) |
|[ get_ancestor(ancestor_type)](../node/get_ancestor/#nodetype) | Gets the first ancestor of the specified [NodeType](../nodetype/).<br>(Inherited from [Node](../node/)) |
|[ get_child(node_type, index, is_deep)](../compositenode/get_child/#nodetype_int_bool) | Returns an Nth child node that matches the specified type.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ get_child_nodes(node_type, is_deep)](../compositenode/get_child_nodes/#nodetype_bool) | Returns a live collection of child nodes that match the specified type.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ get_text()](../node/get_text/#default) | Gets the text of this node and of all its children.<br>(Inherited from [Node](../node/)) |
|[ index_of(child)](../compositenode/index_of/#node) | Returns the index of the specified child node in the child node array.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ insert_after(new_child, ref_child)](../compositenode/insert_after/#node_node) | Inserts the specified node immediately after the specified reference node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ insert_before(new_child, ref_child)](../compositenode/insert_before/#node_node) | Inserts the specified node immediately before the specified reference node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ next_pre_order(root_node)](../node/next_pre_order/#node) | Gets next node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../node/)) |
|[ node_type_to_string(node_type)](../node/node_type_to_string/#nodetype) | A utility method that converts a node type enum value into a user friendly string.<br>(Inherited from [Node](../node/)) |
|[ prepend_child(new_child)](../compositenode/prepend_child/#node) | Adds the specified node to the beginning of the list of child nodes for this node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ previous_pre_order(root_node)](../node/previous_pre_order/#node) | Gets the previous node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../node/)) |
|[ remove()](../node/remove/#default) | Removes itself from the parent.<br>(Inherited from [Node](../node/)) |
|[ remove_all_children()](../compositenode/remove_all_children/#default) | Removes all the child nodes of the current node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ remove_child(old_child)](../compositenode/remove_child/#node) | Removes the specified child node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ remove_smart_tags()](../compositenode/remove_smart_tags/#default) | Removes all [SmartTag](../../aspose.words.markup/smarttag/) descendant nodes of the current node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ select_nodes(xpath)](../compositenode/select_nodes/#str) | Selects a list of nodes matching the XPath expression.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ select_single_node(xpath)](../compositenode/select_single_node/#str) | Selects the first [Node](../node/) that matches the XPath expression.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ to_string(save_format)](../node/to_string/#saveformat) | Exports the content of the node into a string in the specified format.<br>(Inherited from [Node](../node/)) |
|[ to_string(save_options)](../node/to_string/#saveoptions) | Exports the content of the node into a string using the specified save options.<br>(Inherited from [Node](../node/)) |

### Examples

Shows how to create a header and a footer.

```python
doc = aw.Document()
# Create a header and append a paragraph to it. The text in that paragraph
# will appear at the top of every page of this section, above the main body text.
header = aw.HeaderFooter(doc, aw.HeaderFooterType.HEADER_PRIMARY)
doc.first_section.headers_footers.add(header)
para = header.append_paragraph('My header.')
self.assertTrue(header.is_header)
self.assertTrue(para.is_end_of_header_footer)
# Create a footer and append a paragraph to it. The text in that paragraph
# will appear at the bottom of every page of this section, below the main body text.
footer = aw.HeaderFooter(doc, aw.HeaderFooterType.FOOTER_PRIMARY)
doc.first_section.headers_footers.add(footer)
para = footer.append_paragraph('My footer.')
self.assertFalse(footer.is_header)
self.assertTrue(para.is_end_of_header_footer)
self.assertEqual(footer, para.parent_story)
self.assertEqual(footer.parent_section, para.parent_section)
self.assertEqual(footer.parent_section, header.parent_section)
doc.save(file_name=ARTIFACTS_DIR + 'HeaderFooter.Create.docx')
```

Shows how to delete all footers from a document.

```python
doc = aw.Document(MY_DIR + 'Header and footer types.docx')
# Iterate through each section and remove footers of every kind.
for section in doc:
    section = section.as_section()
    # There are three kinds of footer and header types.
    # 1 -  The "First" header/footer, which only appears on the first page of a section.
    footer = section.headers_footers[aw.HeaderFooterType.FOOTER_FIRST]
    if footer is not None:
        footer.remove()
    # 2 -  The "Primary" header/footer, which appears on odd pages.
    footer = section.headers_footers[aw.HeaderFooterType.FOOTER_PRIMARY]
    if footer is not None:
        footer.remove()
    # 3 -  The "Even" header/footer, which appears on even pages.
    footer = section.headers_footers[aw.HeaderFooterType.FOOTER_EVEN]
    if footer is not None:
        footer.remove()
    self.assertEqual(0, len([node for node in section.headers_footers if not node.as_header_footer().is_header]))
doc.save(ARTIFACTS_DIR + 'HeaderFooter.remove_footers.docx')
```

Shows how to replace text in a document's footer.

```python
doc = aw.Document(MY_DIR + 'Footer.docx')
headers_footers = doc.first_section.headers_footers
footer = headers_footers.get_by_header_footer_type(aw.HeaderFooterType.FOOTER_PRIMARY)
options = aw.replacing.FindReplaceOptions()
options.match_case = False
options.find_whole_words_only = False
current_year = date.today().year
footer.range.replace('(C) 2006 Aspose Pty Ltd.', f'Copyright (C) {current_year} by Aspose Pty Ltd.', options)
doc.save(ARTIFACTS_DIR + 'HeaderFooter.replace_text.docx')
```

### See Also

* module [aspose.words](../)
* class [Story](../story/)

