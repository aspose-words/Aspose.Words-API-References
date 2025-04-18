﻿---
title: Section class
linktitle: Section class
articleTitle: Section class
second_title: Aspose.Words for Python
description: "aspose.words.Section class. Represents a single section in a document"
type: docs
weight: 1070
url: /python-net/aspose.words/section/
---

## Section class

Represents a single section in a document.
To learn more, visit the [Working with Sections](https://docs.aspose.com/words/python-net/working-with-sections/) documentation article.




### Remarks

[Section](./) can have one [Body](../body/) and maximum one [HeaderFooter](../headerfooter/)
of each [HeaderFooterType](../headerfootertype/). [Body](../body/) and [HeaderFooter](../headerfooter/) nodes
can be in any order inside [Section](./).

A minimal valid section needs to have [Body](../body/) with one [Paragraph](../paragraph/).

Each section has its own set of properties that specify page size, orientation, margins etc.

You can create a copy of a section using [Node.clone()](../node/clone/#bool). The copy can be inserted into
the same or different document.

To add, insert or remove a whole section including section break and
section properties use methods of the [Document.sections](../document/sections/) object.

To copy and insert just content of the section excluding the section break
and section properties use [Section.append_content()](./append_content/#section) and [Section.prepend_content()](./prepend_content/#section) methods.




**Inheritance:** [Section](./) → [CompositeNode](../compositenode/) → [Node](../node/)

### Constructors
| Name | Description |
| --- | --- |
| [Section(doc)](./__init__/#documentbase) | Initializes a new instance of the Section class. |

### Properties

| Name | Description |
| --- | --- |
| [body](./body/) | Returns the [Body](../body/) child node of the section. |
| [count](../compositenode/count/) | Gets the number of immediate children of this node.<br>(Inherited from [CompositeNode](../compositenode/)) |
| [custom_node_id](../node/custom_node_id/) | Specifies custom node identifier.<br>(Inherited from [Node](../node/)) |
| [document](../node/document/) | Gets the document to which this node belongs.<br>(Inherited from [Node](../node/)) |
| [first_child](../compositenode/first_child/) | Gets the first child of the node.<br>(Inherited from [CompositeNode](../compositenode/)) |
| [has_child_nodes](../compositenode/has_child_nodes/) | Returns ``True`` if this node has any child nodes.<br>(Inherited from [CompositeNode](../compositenode/)) |
| [headers_footers](./headers_footers/) | Provides access to the headers and footers nodes of the section. |
| [is_composite](../node/is_composite/) | Returns ``True`` if this node can contain other nodes.<br>(Inherited from [Node](../node/)) |
| [last_child](../compositenode/last_child/) | Gets the last child of the node.<br>(Inherited from [CompositeNode](../compositenode/)) |
| [next_sibling](../node/next_sibling/) | Gets the node immediately following this node.<br>(Inherited from [Node](../node/)) |
| [node_type](./node_type/) | Returns [NodeType.SECTION](../nodetype/#SECTION). |
| [page_setup](./page_setup/) | Returns an object that represents page setup and section properties. |
| [parent_node](../node/parent_node/) | Gets the immediate parent of this node.<br>(Inherited from [Node](../node/)) |
| [previous_sibling](../node/previous_sibling/) | Gets the node immediately preceding this node.<br>(Inherited from [Node](../node/)) |
| [protected_for_forms](./protected_for_forms/) | True if the section is protected for forms. When a section is protected for forms, users can select and modify text only in form fields in Microsoft Word. |
| [range](../node/range/) | Returns a [Range](../range/) object that represents the portion of a document that is contained in this node.<br>(Inherited from [Node](../node/)) |

### Methods

| Name | Description |
| --- | --- |
|[ accept(visitor)](./accept/#documentvisitor) | Accepts a visitor. |
|[ accept_end(visitor)](../compositenode/accept_end/#documentvisitor) | When implemented in a derived class, calls the VisitXXXEnd method of the specified document visitor.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ accept_start(visitor)](../compositenode/accept_start/#documentvisitor) | When implemented in a derived class, calls the VisitXXXStart method of the specified document visitor.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ append_child(new_child)](../compositenode/append_child/#node) | Adds the specified node to the end of the list of child nodes for this node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ append_content(source_section)](./append_content/#section) | Inserts a copy of content of the source section at the end of this section. |
|[ clear_content()](./clear_content/#default) | Clears the section. |
|[ clear_headers_footers()](./clear_headers_footers/#default) | Clears the headers and footers of this section. |
|[ clear_headers_footers(preserve_watermarks)](./clear_headers_footers/#bool) | Clears the headers and footers of this section. |
|[ clone()](./clone/#default) | Creates a duplicate of this section. |
|[ clone(is_clone_children)](./clone/#bool) | Creates a duplicate of this section. |
|[ delete_header_footer_shapes()](./delete_header_footer_shapes/#default) | Deletes all shapes (drawing objects) from the headers and footers of this section. |
|[ ensure_minimum()](./ensure_minimum/#default) | Ensures that the section has [Section.body](./body/) with one [Paragraph](../paragraph/). |
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
|[ prepend_content(source_section)](./prepend_content/#section) | Inserts a copy of content of the source section at the beginning of this section. |
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
# Call the "RemoveAllChildren" method to remove all those nodes,
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
para.paragraph_format.style_name = 'Heading 1'
para.paragraph_format.alignment = aw.ParagraphAlignment.CENTER
body.append_child(para)
# Finally, add some content to do the document. Create a run,
# set its appearance and contents, and then append it as a child to the paragraph.
run = aw.Run(doc=doc)
run.text = 'Hello World!'
run.font.color = aspose.pydrawing.Color.red
para.append_child(run)
self.assertEqual('Hello World!', doc.get_text().strip())
doc.save(file_name=ARTIFACTS_DIR + 'Section.CreateManually.docx')
```

### See Also

* module [aspose.words](../)
* class [CompositeNode](../compositenode/)

