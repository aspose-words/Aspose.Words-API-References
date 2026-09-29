---
title: LayoutEnumerator.move_first_child method
linktitle: move_first_child method
articleTitle: move_first_child method
second_title: Aspose.Words for Python
description: "LayoutEnumerator.move_first_child method. Moves to the first child entity."
type: docs
weight: 80
url: /sv/python-net/aspose.words.layout/layoutenumerator/move_first_child/
---

## move_first_child() {#default}

Moves to the first child entity.


```python
def move_first_child(self):
    ...
```

### Examples

Shows ways of traversing a document's layout entities (TraverseLayoutForward).

```python
@staticmethod
def _traverse_layout_forward(layout_enumerator, depth):
    while true:
        ExLayout._print_current_entity(layout_enumerator, depth)
        if layout_enumerator.move_first_child():
            ExLayout._traverse_layout_forward(layout_enumerator, depth + 1)
            layout_enumerator.move_parent()
        if layout_enumerator.move_next():
            break

@staticmethod
def _traverse_layout_backward(layout_enumerator, depth):
    while true:
        ExLayout._print_current_entity(layout_enumerator, depth)
        if layout_enumerator.move_last_child():
            ExLayout._traverse_layout_backward(layout_enumerator, depth + 1)
            layout_enumerator.move_parent()
        if layout_enumerator.move_previous():
            break

@staticmethod
def _traverse_layout_forward_logical(layout_enumerator, depth):
    while true:
        ExLayout._print_current_entity(layout_enumerator, depth)
        if layout_enumerator.move_first_child():
            ExLayout._traverse_layout_forward_logical(layout_enumerator, depth + 1)
            layout_enumerator.move_parent()
        if layout_enumerator.move_next_logical():
            break

@staticmethod
def _traverse_layout_backward_logical(layout_enumerator, depth):
    while true:
        ExLayout._print_current_entity(layout_enumerator, depth)
        if layout_enumerator.move_last_child():
            ExLayout._traverse_layout_backward_logical(layout_enumerator, depth + 1)
            layout_enumerator.move_parent()
        if layout_enumerator.move_previous_logical():
            break

@staticmethod
def _print_current_entity(layout_enumerator, indent):
    tabs = '\t' * indent
    print(f'{tabs}-> Entity type: {layout_enumerator.type}' if layout_enumerator.kind == '' else f'{tabs}-> Entity type & kind: {layout_enumerator.type}, {layout_enumerator.kind}')
    # Endast spans kan innehålla text.
    if layout_enumerator.type == aw.LayoutEntityType.SPAN:
        print(f'{tabs}   Span contents: "{layout_enumerator.text}"')
        le_rect = layout_enumerator.rectangle
        print(f'{tabs}   Rectangle dimensions {le_rect.width}x{le_rect.height}, X={le_rect.x} Y={le_rect.y}')
        print(f'{tabs}   Page {layout_enumerator.page_index}')
```

Shows ways of traversing a document's layout entities.

```python
def layout_enumerator_example():
    # Öppna ett dokument som innehåller en mängd olika layout-entiteter.
    # Layout-entiteter är sidor, celler, rader, linjer och andra objekt som ingår i LayoutEntityType-enum.
    # Varje layout-entitet har ett rektangulärt utrymme som den upptar i dokumentkroppen.
    doc = aw.Document(MY_DIR + 'Layout entities.docx')
    # Skapa en enumerator som kan traversera dessa entiteter som ett träd.
    layout_enumerator = aw.layout.LayoutEnumerator(doc)
    self.assertEqual(doc, layout_enumerator.document)
    layout_enumerator.move_parent(aw.layout.LayoutEntityType.PAGE)
    self.assertEqual(aw.layout.LayoutEntityType.PAGE, layout_enumerator.type)
    with self.assertRaises(Exception):
        print(layout_enumerator.text)
    # Vi kan anropa den här metoden för att säkerställa att enumeratorn befinner sig på den första layout-entiteten.
    layout_enumerator.reset()
    # Det finns två ordningar som bestämmer hur layout-enumeratorn fortsätter att traversera layout-entiteter
    # när den stöter på entiteter som sträcker sig över flera sidor.
    # 1 -  I visuell ordning:
    # När du går igenom en enhets barn som sträcker sig över flera sidor,
    # sidlayouten har företräde, och vi går till andra barn-element på den här sidan och undviker de på nästa.
    print('Traversing from first to last, elements between pages separated:')
    traverse_layout_forward(layout_enumerator, 1)
    # Vår enumerator är nu i slutet av samlingen. Vi kan traversera layout‑entiteterna bakåt för att gå tillbaka till början.
    print('Traversing from last to first, elements between pages separated:')
    traverse_layout_backward(layout_enumerator, 1)
    # 2 -  I logisk ordning:
    # När du går igenom en enhets barn som sträcker sig över flera sidor,
    # enumeratorn kommer att flytta mellan sidor för att traversera alla barn‑entiteter.
    print('Traversing from first to last, elements between pages mixed:')
    traverse_layout_forward_logical(layout_enumerator, 1)
    print('Traversing from last to first, elements between pages mixed:')
    traverse_layout_backward_logical(layout_enumerator, 1)

def traverse_layout_forward(layout_enumerator: aw.layout.LayoutEnumerator, depth: int):
    """Enumerate through layout_enumerator's layout entity collection front-to-back,
    in a depth-first manner, and in the "Visual" order."""
    while True:
        print_current_entity(layout_enumerator, depth)
        if layout_enumerator.move_first_child():
            traverse_layout_forward(layout_enumerator, depth + 1)
            layout_enumerator.move_parent()
        if not layout_enumerator.move_next():
            break

def traverse_layout_backward(layout_enumerator: aw.layout.LayoutEnumerator, depth: int):
    """Enumerate through layout_enumerator's layout entity collection back-to-front,
    in a depth-first manner, and in the "Visual" order."""
    while True:
        print_current_entity(layout_enumerator, depth)
        if layout_enumerator.move_last_child():
            traverse_layout_backward(layout_enumerator, depth + 1)
            layout_enumerator.move_parent()
        if not layout_enumerator.move_previous():
            break

def traverse_layout_forward_logical(layout_enumerator: aw.layout.LayoutEnumerator, depth: int):
    """Enumerate through layout_enumerator's layout entity collection front-to-back,
    in a depth-first manner, and in the "Logical" order."""
    while True:
        print_current_entity(layout_enumerator, depth)
        if layout_enumerator.move_first_child():
            traverse_layout_forward_logical(layout_enumerator, depth + 1)
            layout_enumerator.move_parent()
        if not layout_enumerator.move_next_logical():
            break

def traverse_layout_backward_logical(layout_enumerator: aw.layout.LayoutEnumerator, depth: int):
    """Enumerate through layout_enumerator's layout entity collection back-to-front,
    in a depth-first manner, and in the "Logical" order."""
    while True:
        print_current_entity(layout_enumerator, depth)
        if layout_enumerator.move_last_child():
            traverse_layout_backward_logical(layout_enumerator, depth + 1)
            layout_enumerator.move_parent()
        if not layout_enumerator.move_previous_logical():
            break

def print_current_entity(layout_enumerator: aw.layout.LayoutEnumerator, indent: int):
    """Print information about layout_enumerator's current entity to the console, while indenting the text with tab characters
    based on its depth relative to the root node that we provided in the constructor LayoutEnumerator instance.
    The rectangle that we process at the end represents the area and location that the entity takes up in the document."""
    tabs = '\t' * indent
    if layout_enumerator.kind == '':
        print(f'{tabs}-> Entity type: {layout_enumerator.type}')
    else:
        print(f'{tabs}-> Entity type & kind: {layout_enumerator.type}, {layout_enumerator.kind}')
    # Endast spans kan innehålla text.
    if layout_enumerator.type == aw.layout.LayoutEntityType.SPAN:
        print(f'{tabs}   Span contents: "{layout_enumerator.text}"')
    le_rect = layout_enumerator.rectangle
    print(f'{tabs}   Rectangle dimensions {le_rect.width}x{le_rect.height}, X={le_rect.x} Y={le_rect.y}')
    print(f'{tabs}   Page {layout_enumerator.page_index}')
```

### See Also

* module [aspose.words.layout](../../)
* class [LayoutEnumerator](../)

