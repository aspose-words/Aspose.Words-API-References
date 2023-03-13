﻿---
title: Paragraph class
second_title: Aspose.Words for Python via .NET API Reference
description: "Represents a paragraph of text"
type: docs
weight: 840
url: /python-net/aspose.words/paragraph/
---

## Paragraph class

Represents a paragraph of text.
To learn more, visit the [Working with Paragraphs](https://docs.aspose.com/words/python-net/working-with-paragraphs/) documentation article.




[Paragraph](./) is a block-level node and can be a child of classes derived from
[Story](../story/) or [InlineStory](../inlinestory/).

[Paragraph](./) can contain any number of inline-level nodes and bookmarks.

The complete list of child nodes that can occur inside a paragraph consists of
[BookmarkStart](../bookmarkstart/), [BookmarkEnd](../bookmarkend/),
[FieldStart](../../aspose.words.fields/fieldstart/), [FieldSeparator](../../aspose.words.fields/fieldseparator/),
[FieldEnd](../../aspose.words.fields/fieldend/), [FormField](../../aspose.words.fields/formfield/),
[Comment](../comment/), [Footnote](../../aspose.words.notes/footnote/),
[Run](../run/), [SpecialChar](../specialchar/),
[Shape](../../aspose.words.drawing/shape/), [GroupShape](../../aspose.words.drawing/groupshape/),
[SmartTag](../../aspose.words.markup/smarttag/).

A valid paragraph in Microsoft Word always ends with a paragraph break character and
a minimal valid paragraph consists just of a paragraph break. The [Paragraph](./)
class automatically appends the appropriate paragraph break character at the end
and this character is not part of the child nodes of the [Paragraph](./), therefore
a [Paragraph](./) can be empty.

Do not include the end of paragraph [ControlChar.PARAGRAPH_BREAK](../controlchar/PARAGRAPH_BREAK/)
or end of cell [ControlChar.CELL](../controlchar/CELL/) characters inside the text of
the paragraph as it might make the paragraph invalid when the document is opened in Microsoft Word.




**Inheritance:** [Paragraph](./) → [CompositeNode](../compositenode/) → [Node](../node/)

### Constructors
| Name | Description |
| --- | --- |
| [Paragraph(doc)](./__init__/#documentbase) | Initializes a new instance of the [Paragraph](./) class. |

### Properties

| Name | Description |
| --- | --- |
| [break_is_style_separator](./break_is_style_separator/) | True if this paragraph break is a Style Separator. A style separator allows one paragraph to consist of parts that have different paragraph styles. |
| [child_nodes](../compositenode/child_nodes/) | Gets all immediate child nodes of this node.<br>(Inherited from [CompositeNode](../compositenode/)) |
| [count](../compositenode/count/) | Gets the number of immediate children of this node.<br>(Inherited from [CompositeNode](../compositenode/)) |
| [custom_node_id](../node/custom_node_id/) | Specifies custom node identifier.<br>(Inherited from [Node](../node/)) |
| [document](../node/document/) | Gets the document to which this node belongs.<br>(Inherited from [Node](../node/)) |
| [first_child](../compositenode/first_child/) | Gets the first child of the node.<br>(Inherited from [CompositeNode](../compositenode/)) |
| [frame_format](./frame_format/) | Provides access to the frame formatting properties. |
| [has_child_nodes](../compositenode/has_child_nodes/) | Returns ``True`` if this node has any child nodes.<br>(Inherited from [CompositeNode](../compositenode/)) |
| [is_composite](../node/is_composite/) | Returns ``True`` if this node can contain other nodes.<br>(Inherited from [Node](../node/)) |
| [is_delete_revision](./is_delete_revision/) | Returns true if this object was deleted in Microsoft Word while change tracking was enabled. |
| [is_end_of_cell](./is_end_of_cell/) | True if this paragraph is the last paragraph in a [Cell](../../aspose.words.tables/cell/); false otherwise. |
| [is_end_of_document](./is_end_of_document/) | True if this paragraph is the last paragraph in the last section of the document. |
| [is_end_of_header_footer](./is_end_of_header_footer/) | True if this paragraph is the last paragraph in the [HeaderFooter](../headerfooter/) (main text story) of a [Section](../section/); false otherwise. |
| [is_end_of_section](./is_end_of_section/) | True if this paragraph is the last paragraph in the [Body](../body/) (main text story) of a [Section](../section/); false otherwise. |
| [is_format_revision](./is_format_revision/) | Returns true if formatting of the object was changed in Microsoft Word while change tracking was enabled. |
| [is_in_cell](./is_in_cell/) | True if this paragraph is an immediate child of [Cell](../../aspose.words.tables/cell/); false otherwise. |
| [is_insert_revision](./is_insert_revision/) | Returns true if this object was inserted in Microsoft Word while change tracking was enabled. |
| [is_list_item](./is_list_item/) | True when the paragraph is an item in a bulleted or numbered list in original revision. |
| [is_move_from_revision](./is_move_from_revision/) | Returns ``True`` if this object was moved (deleted) in Microsoft Word while change tracking was enabled. |
| [is_move_to_revision](./is_move_to_revision/) | Returns ``True`` if this object was moved (inserted) in Microsoft Word while change tracking was enabled. |
| [last_child](../compositenode/last_child/) | Gets the last child of the node.<br>(Inherited from [CompositeNode](../compositenode/)) |
| [list_format](./list_format/) | Provides access to the list formatting properties of the paragraph. |
| [list_label](./list_label/) | Gets a [Paragraph.list_label](./list_label/) object that provides access to list numbering value and formatting for this paragraph. |
| [next_sibling](../node/next_sibling/) | Gets the node immediately following this node.<br>(Inherited from [Node](../node/)) |
| [node_type](./node_type/) | Returns [NodeType.PARAGRAPH](../nodetype/#PARAGRAPH). |
| [paragraph_break_font](./paragraph_break_font/) | Provides access to the font formatting of the paragraph break character. |
| [paragraph_format](./paragraph_format/) | Provides access to the paragraph formatting properties. |
| [parent_node](../node/parent_node/) | Gets the immediate parent of this node.<br>(Inherited from [Node](../node/)) |
| [parent_section](./parent_section/) | Retrieves the parent [Section](../section/) of the paragraph. |
| [parent_story](./parent_story/) | Retrieves the parent section-level story that can be [Body](../body/) or [HeaderFooter](../headerfooter/). |
| [previous_sibling](../node/previous_sibling/) | Gets the node immediately preceding this node.<br>(Inherited from [Node](../node/)) |
| [range](../node/range/) | Returns a [Range](../range/) object that represents the portion of a document that is contained in this node.<br>(Inherited from [Node](../node/)) |
| [runs](./runs/) | Provides access to the typed collection of pieces of text inside the paragraph. |

### Methods

| Name | Description |
| --- | --- |
|[ accept(visitor)](./accept/#documentvisitor) | Accepts a visitor. |
|[ append_child(new_child)](../compositenode/append_child/#node) | Adds the specified node to the end of the list of child nodes for this node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ append_field(field_type, update_field)](./append_field/#fieldtype_bool) | Appends a field to this paragraph. |
|[ append_field(field_code)](./append_field/#str) | Appends a field to this paragraph. |
|[ append_field(field_code, field_value)](./append_field/#str_str) | Appends a field to this paragraph. |
|[ clone(is_clone_children)](../node/clone/#bool) | Creates a duplicate of the node.<br>(Inherited from [Node](../node/)) |
|[ get_ancestor(ancestor_type)](../node/get_ancestor/#unknown) | Gets the first ancestor of the specified object type.<br>(Inherited from [Node](../node/)) |
|[ get_ancestor(ancestor_type)](../node/get_ancestor/#nodetype) | Gets the first ancestor of the specified [NodeType](../nodetype/).<br>(Inherited from [Node](../node/)) |
|[ get_child(node_type, index, is_deep)](../compositenode/get_child/#nodetype_int_bool) | Returns an Nth child node that matches the specified type.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ get_child_nodes(node_type, is_deep)](../compositenode/get_child_nodes/#nodetype_bool) | Returns a live collection of child nodes that match the specified type.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ get_effective_tab_stops()](./get_effective_tab_stops/#default) | Returns array of all tab stops applied to this paragraph, including applied indirectly by styles or lists. |
|[ get_text()](./get_text/#default) | Gets the text of this paragraph including the end of paragraph character. |
|[ index_of(child)](../compositenode/index_of/#node) | Returns the index of the specified child node in the child node array.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ insert_after(new_child, ref_child)](../compositenode/insert_after/#node_node) | Inserts the specified node immediately after the specified reference node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ insert_before(new_child, ref_child)](../compositenode/insert_before/#node_node) | Inserts the specified node immediately before the specified reference node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ insert_field(field_type, update_field, ref_node, is_after)](./insert_field/#fieldtype_bool_node_bool) | Inserts a field into this paragraph. |
|[ insert_field(field_code, ref_node, is_after)](./insert_field/#str_node_bool) | Inserts a field into this paragraph. |
|[ insert_field(field_code, field_value, ref_node, is_after)](./insert_field/#str_str_node_bool) | Inserts a field into this paragraph. |
|[ join_runs_with_same_formatting()](./join_runs_with_same_formatting/#default) | Joins runs with the same formatting in the paragraph. |
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

Shows how to construct an Aspose.Words document by hand.

```python
doc = aw.Document()

# A blank document contains one section, one body and one paragraph.
# Call the "remove_all_children" method to remove all those nodes,
# and end up with a document node with no children.
doc.remove_all_children()

# This document now has no composite child nodes that we can add content to.
# If we wish to edit it, we will need to repopulate its node collection.
# First, create a new section, and then append it as a child to the root document node.
section = aw.Section(doc)
doc.append_child(section)

# Set some page setup properties for the section.
section.page_setup.section_start = aw.SectionStart.NEW_PAGE
section.page_setup.paper_size = aw.PaperSize.LETTER

# A section needs a body, which will contain and display all its contents
# on the page between the section's header and footer.
body = aw.Body(doc)
section.append_child(body)

# Create a paragraph, set some formatting properties, and then append it as a child to the body.
para = aw.Paragraph(doc)

para.paragraph_format.style_name = "Heading 1"
para.paragraph_format.alignment = aw.ParagraphAlignment.CENTER

body.append_child(para)

# Finally, add some content to do the document. Create a run,
# set its appearance and contents, and then append it as a child to the paragraph.
run = aw.Run(doc)
run.text = "Hello World!"
run.font.color = drawing.Color.red
para.append_child(run)

self.assertEqual("Hello World!", doc.get_text().strip())

doc.save(ARTIFACTS_DIR + "Section.create_manually.docx")
```

### See Also

* module [aspose.words](../)
* class [CompositeNode](../compositenode/)

