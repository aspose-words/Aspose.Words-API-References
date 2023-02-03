---
title: FieldStart class
second_title: Aspose.Words for Python via .NET API Reference
description: "Represents a start of a Word field in a document"
type: docs
weight: 970
url: /python-net/aspose.words.fields/fieldstart/
---

## FieldStart class

Represents a start of a Word field in a document.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/python-net/working-with-fields/) documentation article.




[FieldStart](./) is an inline-level node and represented by the
[ControlChar.FIELD_START_CHAR](../../aspose.words/controlchar/FIELD_START_CHAR/) control character in the document.

[FieldStart](./) can only be a child of [Paragraph](../../aspose.words/paragraph/).

A complete field in a Microsoft Word document is a complex structure consisting of
a field start character, field code, field separator character, field result
and field end character. Some fields only have field start, field code and field end.

To easily insert a new field into a document, use the [DocumentBuilder.insert_field()](../../aspose.words/documentbuilder/insert_field/#str)
method.




**Inheritance:** [FieldStart](./) → [FieldChar](../fieldchar/) → [SpecialChar](../../aspose.words/specialchar/) → [Inline](../../aspose.words/inline/) → [Node](../../aspose.words/node/)

### Properties

| Name | Description |
| --- | --- |
| [custom_node_id](../../aspose.words/node/custom_node_id/) | Specifies custom node identifier.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [document](../../aspose.words/node/document/) | Gets the document to which this node belongs.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [field_data](./field_data/) | Gets custom field data which is associated with the field. |
| [field_type](../fieldchar/field_type/) | Returns the type of the field.<br>(Inherited from [FieldChar](../fieldchar/)) |
| [font](../../aspose.words/inline/font/) | Provides access to the font formatting of this object.<br>(Inherited from [Inline](../../aspose.words/inline/)) |
| [is_composite](../../aspose.words/node/is_composite/) | Returns ``True`` if this node can contain other nodes.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [is_delete_revision](../../aspose.words/inline/is_delete_revision/) | Returns true if this object was deleted in Microsoft Word while change tracking was enabled.<br>(Inherited from [Inline](../../aspose.words/inline/)) |
| [is_dirty](../fieldchar/is_dirty/) | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.<br>(Inherited from [FieldChar](../fieldchar/)) |
| [is_format_revision](../../aspose.words/inline/is_format_revision/) | Returns true if formatting of the object was changed in Microsoft Word while change tracking was enabled.<br>(Inherited from [Inline](../../aspose.words/inline/)) |
| [is_insert_revision](../../aspose.words/inline/is_insert_revision/) | Returns true if this object was inserted in Microsoft Word while change tracking was enabled.<br>(Inherited from [Inline](../../aspose.words/inline/)) |
| [is_locked](../fieldchar/is_locked/) | Gets or sets whether the parent field is locked (should not recalculate its result).<br>(Inherited from [FieldChar](../fieldchar/)) |
| [is_move_from_revision](../../aspose.words/inline/is_move_from_revision/) | Returns ``True`` if this object was moved (deleted) in Microsoft Word while change tracking was enabled.<br>(Inherited from [Inline](../../aspose.words/inline/)) |
| [is_move_to_revision](../../aspose.words/inline/is_move_to_revision/) | Returns ``True`` if this object was moved (inserted) in Microsoft Word while change tracking was enabled.<br>(Inherited from [Inline](../../aspose.words/inline/)) |
| [next_sibling](../../aspose.words/node/next_sibling/) | Gets the node immediately following this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [node_type](./node_type/) | Returns [NodeType.FIELD_START](../../aspose.words/nodetype/#FIELD_START). |
| [parent_node](../../aspose.words/node/parent_node/) | Gets the immediate parent of this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [parent_paragraph](../../aspose.words/inline/parent_paragraph/) | Retrieves the parent [Paragraph](../../aspose.words/paragraph/) of this node.<br>(Inherited from [Inline](../../aspose.words/inline/)) |
| [previous_sibling](../../aspose.words/node/previous_sibling/) | Gets the node immediately preceding this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [range](../../aspose.words/node/range/) | Returns a [Range](../../aspose.words/range/) object that represents the portion of a document that is contained in this node.<br>(Inherited from [Node](../../aspose.words/node/)) |

### Methods

| Name | Description |
| --- | --- |
|[ accept(visitor)](./accept/#documentvisitor) | Accepts a visitor. |
|[ clone(is_clone_children)](../../aspose.words/node/clone/#bool) | Creates a duplicate of the node.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ get_ancestor(ancestor_type)](../../aspose.words/node/get_ancestor/#unknown) | Gets the first ancestor of the specified object type.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ get_ancestor(ancestor_type)](../../aspose.words/node/get_ancestor/#nodetype) | Gets the first ancestor of the specified [NodeType](../../aspose.words/nodetype/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ get_field()](../fieldchar/get_field/#default) | Returns a field for the field char.<br>(Inherited from [FieldChar](../fieldchar/)) |
|[ get_text()](../../aspose.words/node/get_text/#default) | Gets the text of this node and of all its children.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ next_pre_order(root_node)](../../aspose.words/node/next_pre_order/#node) | Gets next node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ node_type_to_string(node_type)](../../aspose.words/node/node_type_to_string/#nodetype) | A utility method that converts a node type enum value into a user friendly string.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ previous_pre_order(root_node)](../../aspose.words/node/previous_pre_order/#node) | Gets the previous node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ remove()](../../aspose.words/node/remove/#default) | Removes itself from the parent.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ to_string(save_format)](../../aspose.words/node/to_string/#saveformat) | Exports the content of the node into a string in the specified format.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ to_string(save_options)](../../aspose.words/node/to_string/#saveoptions) | Exports the content of the node into a string using the specified save options.<br>(Inherited from [Node](../../aspose.words/node/)) |

### Examples

Shows how to find all hyperlinks in a Word document, and then change their URLs and display names.

```python
class ExReplaceHyperlinks(ApiExampleBase):

    def test_fields(self):

        doc = aw.Document(MY_DIR + "Hyperlinks.docx")

        # Hyperlinks in a Word documents are fields. To begin looking for hyperlinks, we must first find all the fields.
        # Use the "select_nodes" method to find all the fields in the document via an XPath.
        field_starts = doc.select_nodes("//FieldStart")

        for field_start in field_starts:
            field_start = field_start.as_field_start()

            if field_start.field_type == aw.fields.FieldType.FIELD_HYPERLINK:
                hyperlink = Hyperlink(field_start)

                # Hyperlinks that link to bookmarks do not have URLs.
                if hyperlink.is_local:
                    continue

                # Give each URL hyperlink a new URL and name.
                hyperlink.target = "http://www.aspose.com"
                hyperlink.name = "Aspose - The .NET & Java Component Publisher"

        doc.save(ARTIFACTS_DIR + "ReplaceHyperlinks.fields.docx")


class Hyperlink:
    """HYPERLINK fields contain and display hyperlinks in the document body. A field in Aspose.Words
    consists of several nodes, and it might be difficult to work with all those nodes directly.
    This implementation will work only if the hyperlink code and name each consist of only one Run node.

    The node structure for fields is as follows:

    [FieldStart][Run - field code][FieldSeparator][Run - field result][FieldEnd]

    Below are two example field codes of HYPERLINK fields:
    HYPERLINK "url"
    HYPERLINK \\l "bookmark name"

    A field's "result" property contains text that the field displays in the document body to the user."""
    def __init__(self, field_start: aw.fields.FieldStart):

        if field_start is None:
            raise ValueError("field_start")
        if field_start.field_type != aw.fields.FieldType.FIELD_HYPERLINK:
            raise ValueError("Field start type must be FieldHyperlink.")

        self.field_start = field_start

        # Find the field separator node.
        self.field_separator = Hyperlink.find_next_sibling(self.field_start, aw.NodeType.FIELD_SEPARATOR)
        if self.field_separator is None:
            raise Exception("Cannot find field separator.")

        # Normally, we can always find the field's end node, but the example document
        # contains a paragraph break inside a hyperlink, which puts the field end
        # in the next paragraph. It will be much more complicated to handle fields which span several
        # paragraphs correctly. In this case allowing field end to be null is enough.
        self.field_end = Hyperlink.find_next_sibling(self.field_separator, aw.NodeType.FIELD_END)

        # Field code looks something like "HYPERLINK "http:\\www.myurl.com"", but it can consist of several runs.
        field_code = Hyperlink.get_text_same_parent(self.field_start.next_sibling, self.field_separator)

        pattern = r"""
        \S+        # One or more non spaces HYPERLINK or other word in other languages.
        \s+        # One or more spaces.
        (?:""\s+)? # Non-capturing optional "" and one or more spaces.
        (\\l\s+)?  # Optional \l flag followed by one or more spaces.
        "          # One apostrophe.
        ([^"]+)    # One or more characters, excluding the apostrophe (hyperlink target).
        "          # One closing apostrophe.
        """

        match = re.match(pattern, field_code.strip(), re.VERBOSE)

        # The hyperlink is local if \l is present in the field code.
        self._is_local = len(match.group(2)) > 0
        self._target = match.groups(3)

    @property
    def name(self) -> str:
        """Gets the display name of the hyperlink."""
        return Hyperlink.GetTextSameParent(self.field_separator, self.field_end)

    @name.setter
    def name(self, value: str):
        """Sets the display name of the hyperlink."""

        # Hyperlink display name is stored in the field result, which is a Run
        # node between field separator and field end.
        field_result = self.field_separator.next_sibling.as_run()
        field_result.text = value

        # If the field result consists of more than one run, delete these runs.
        Hyperlink.remove_same_parent(field_result.next_sibling, self.field_end)

    @property
    def target(self) -> str:
        """Gets the target URL or bookmark name of the hyperlink."""
        return self._target

    @target.setter
    def target(self, value: str) -> str:
        """Sets the target URL or bookmark name of the hyperlink."""
        self._target = value
        self.update_field_code()

    @property
    def is_local(self) -> bool:
        """True if the hyperlinks target is a bookmark inside the document. False if the hyperlink is a URL."""
        return self._is_local

    @is_local.setter
    def is_local(self, value: bool):
        self._is_local = value
        self.update_field_code()

    def update_field_code(self):

        # A field's field code is in a Run node between the field's start node and field separator.
        field_code = self.field_start.next_sibling.as_run()
        field_code.text = 'HYPERLINK {0}"{1}"'.format(
            "\\l " if self.is_local else "", self.target)

        # If the field code consists of more than one run, delete these runs.
        Hyperlink.remove_same_parent(field_code.next_sibling, self.field_separator)

    @staticmethod
    def find_next_sibling(start_node: aw.Node, node_type: aw.NodeType) -> aw.Node:
        """Goes through siblings starting from the start node until it finds a node of the specified type or None."""

        node = start_node
        while node is not None:
            if node.node_type == node_type:
                return node

            node = node.next_sibling

        return None

    @staticmethod
    def get_text_same_parent(start_node: aw.Node, end_node: aw.Node) -> str:
        """Retrieves text from start up to but not including the end node."""

        if end_node is not None and start_node.parent_node != end_node.parent_node:
            raise ValueError("Start and end nodes are expected to have the same parent.")

        text = ''
        child = start_node
        while child != end_node:
            text += child.get_text()
            child = child.next_sibling

        return text

    @staticmethod
    def remove_same_parent(start_node: aw.Node, end_node: aw.Node):
        """Removes nodes from start up to but not including the end node.
        Assumes that the start and end nodes have the same parent."""

        if end_node is not None and start_node.parent_node != end_node.parent_node:
            raise ValueError("Start and end nodes are expected to have the same parent.")

        cur_child = start_node
        while cur_child is not None and cur_child != end_node:
            next_child = cur_child.next_sibling
            cur_child.remove()
            cur_child = next_child
```

### See Also

* module [aspose.words.fields](../)
* class [FieldChar](../fieldchar/)

