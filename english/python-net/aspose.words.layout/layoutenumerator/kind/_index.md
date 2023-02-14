---
title: kind property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets the kind of the current entity"
type: docs
weight: 30
url: /python-net/aspose.words.layout/layoutenumerator/kind/
---

## LayoutEnumerator.kind property

Gets the kind of the current entity. This can be an empty string but never ``None``.


This is a more specific type of the current entity, e.g. bookmark span has [LayoutEntityType.SPAN](../../layoutentitytype/#SPAN) type and
may have either a BOOKMARKSTART or BOOKMARKEND kind.


### Examples

Shows ways of traversing a document's layout entities.

```python
def test_layout_enumerator(self):

    # Open a document that contains a variety of layout entities.
    # Layout entities are pages, cells, rows, lines, and other objects included in the LayoutEntityType enum.
    # Each layout entity has a rectangular space that it occupies in the document body.
    doc = aw.Document(MY_DIR + "Layout entities.docx")

    # Create an enumerator that can traverse these entities like a tree.
    layout_enumerator = aw.layout.LayoutEnumerator(doc)

    self.assertEqual(doc, layout_enumerator.document)

    layout_enumerator.move_parent(aw.layout.LayoutEntityType.PAGE)

    self.assertEqual(aw.layout.LayoutEntityType.PAGE, layout_enumerator.type)
    with self.assertRaises(Exception):
        print(layout_enumerator.text)

    # We can call this method to make sure that the enumerator will be at the first layout entity.
    layout_enumerator.reset()

    # There are two orders that determine how the layout enumerator continues traversing layout entities
    # when it encounters entities that span across multiple pages.
    # 1 -  In visual order:
    # When moving through an entity's children that span multiple pages,
    # page layout takes precedence, and we move to other child elements on this page and avoid the ones on the next.
    print("Traversing from first to last, elements between pages separated:")
    ExLayout.traverse_layout_forward(layout_enumerator, 1)

    # Our enumerator is now at the end of the collection. We can traverse the layout entities backwards to go back to the beginning.
    print("Traversing from last to first, elements between pages separated:")
    ExLayout.traverse_layout_backward(layout_enumerator, 1)

    # 2 -  In logical order:
    # When moving through an entity's children that span multiple pages,
    # the enumerator will move between pages to traverse all the child entities.
    print("Traversing from first to last, elements between pages mixed:")
    ExLayout.traverse_layout_forward_logical(layout_enumerator, 1)

    print("Traversing from last to first, elements between pages mixed:")
    ExLayout.traverse_layout_backward_logical(layout_enumerator, 1)

@staticmethod
def traverse_layout_forward(layout_enumerator: aw.layout.LayoutEnumerator, depth: int):
    """Enumerate through layout_enumerator's layout entity collection front-to-back,
    in a depth-first manner, and in the "Visual" order."""

    while True:
        ExLayout.print_current_entity(layout_enumerator, depth)

        if layout_enumerator.move_first_child():
            ExLayout.traverse_layout_forward(layout_enumerator, depth + 1)
            layout_enumerator.move_parent()

        if not layout_enumerator.move_next():
            break

@staticmethod
def traverse_layout_backward(layout_enumerator: aw.layout.LayoutEnumerator, depth: int):
    """Enumerate through layout_enumerator's layout entity collection back-to-front,
    in a depth-first manner, and in the "Visual" order."""

    while True:
        ExLayout.print_current_entity(layout_enumerator, depth)

        if layout_enumerator.move_last_child():
            ExLayout.traverse_layout_backward(layout_enumerator, depth + 1)
            layout_enumerator.move_parent()

        if not layout_enumerator.move_previous():
            break

@staticmethod
def traverse_layout_forward_logical(layout_enumerator: aw.layout.LayoutEnumerator, depth: int):
    """Enumerate through layout_enumerator's layout entity collection front-to-back,
    in a depth-first manner, and in the "Logical" order."""

    while True:
        ExLayout.print_current_entity(layout_enumerator, depth)

        if layout_enumerator.move_first_child():
            ExLayout.traverse_layout_forward_logical(layout_enumerator, depth + 1)
            layout_enumerator.move_parent()

        if not layout_enumerator.move_next_logical():
            break

@staticmethod
def traverse_layout_backward_logical(layout_enumerator: aw.layout.LayoutEnumerator, depth: int):
    """Enumerate through layout_enumerator's layout entity collection back-to-front,
    in a depth-first manner, and in the "Logical" order."""

    while True:
        ExLayout.print_current_entity(layout_enumerator, depth)

        if layout_enumerator.move_last_child():
            ExLayout.traverse_layout_backward_logical(layout_enumerator, depth + 1)
            layout_enumerator.move_parent()

        if not layout_enumerator.move_previous_logical():
            break

@staticmethod
def print_current_entity(layout_enumerator: aw.layout.LayoutEnumerator, indent: int):
    """Print information about layout_enumerator's current entity to the console, while indenting the text with tab characters
    based on its depth relative to the root node that we provided in the constructor LayoutEnumerator instance.
    The rectangle that we process at the end represents the area and location that the entity takes up in the document."""

    tabs = "\t" * indent

    if layout_enumerator.kind == "":
        print(f"{tabs}-> Entity type: {layout_enumerator.type}")
    else:
        print(f"{tabs}-> Entity type & kind: {layout_enumerator.type}, {layout_enumerator.kind}")

    # Only spans can contain text.
    if layout_enumerator.type == aw.layout.LayoutEntityType.SPAN:
        print(f"{tabs}   Span contents: \"{layout_enumerator.text}\"")

    le_rect = layout_enumerator.rectangle
    print(f"{tabs}   Rectangle dimensions {le_rect.width}x{le_rect.height}, X={le_rect.x} Y={le_rect.y}")
    print(f"{tabs}   Page {layout_enumerator.page_index}")
```

### See Also

* module [aspose.words.layout](../../)
* class [LayoutEnumerator](../)

