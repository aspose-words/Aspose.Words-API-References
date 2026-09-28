---
title: LayoutEnumerator.move_next_logical method
linktitle: move_next_logical method
articleTitle: move_next_logical method
second_title: Aspose.Words for Python
description: "LayoutEnumerator.move_next_logical method. Moves to the next sibling entity in a logical order."
type: docs
weight: 110
url: /de/python-net/aspose.words.layout/layoutenumerator/move_next_logical/
---

## move_next_logical() {#default}

Moves to the next sibling entity in a logical order.

When iterating lines of a paragraph broken across pages this method
will move to the next line even if it resides on another page.


```python
def move_next_logical(self):
    ...
```

### Remarks

Note that all [LayoutEntityType.SPAN](../../layoutentitytype/#SPAN) entities are linked together thus if Aspose.Words.Layout.LayoutEnumerator.Current
entity is span repeated calling of this method will iterates complete story of the document.



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
    # Nur Spans können Text enthalten.
    if layout_enumerator.type == aw.LayoutEntityType.SPAN:
        print(f'{tabs}   Span contents: "{layout_enumerator.text}"')
        le_rect = layout_enumerator.rectangle
        print(f'{tabs}   Rectangle dimensions {le_rect.width}x{le_rect.height}, X={le_rect.x} Y={le_rect.y}')
        print(f'{tabs}   Page {layout_enumerator.page_index}')
```

Shows ways of traversing a document's layout entities.

```python
def layout_enumerator_example():
    # Öffnen Sie ein Dokument, das eine Vielzahl von Layout‑Entitäten enthält.
    # Layout‑Entitäten sind Seiten, Zellen, Zeilen, Linien und andere Objekte, die im LayoutEntityType‑Enum enthalten sind.
    # Jede Layout‑Entität hat einen rechteckigen Raum, den sie im Dokumentkörper einnimmt.
    doc = aw.Document(MY_DIR + 'Layout entities.docx')
    # Erstellen Sie einen Enumerator, der diese Entitäten wie einen Baum durchlaufen kann.
    layout_enumerator = aw.layout.LayoutEnumerator(doc)
    self.assertEqual(doc, layout_enumerator.document)
    layout_enumerator.move_parent(aw.layout.LayoutEntityType.PAGE)
    self.assertEqual(aw.layout.LayoutEntityType.PAGE, layout_enumerator.type)
    with self.assertRaises(Exception):
        print(layout_enumerator.text)
    # Wir können diese Methode aufrufen, um sicherzustellen, dass sich der Enumerator beim ersten Layout‑Entität befindet.
    layout_enumerator.reset()
    # Es gibt zwei Reihenfolgen, die bestimmen, wie der Layout‑Enumerator das Durchlaufen von Layout‑Entitäten fortsetzt
    # wenn er auf Entitäten trifft, die sich über mehrere Seiten erstrecken.
    # 1 -  In visueller Reihenfolge:
    # Beim Durchlaufen der Kindobjekte einer Entität, die sich über mehrere Seiten erstrecken,
    # Das Seitenlayout hat Vorrang, und wir wechseln zu anderen Kind-Elementen auf dieser Seite und vermeiden die auf der nächsten.
    print('Traversing from first to last, elements between pages separated:')
    traverse_layout_forward(layout_enumerator, 1)
    # Unser Enumerator befindet sich jetzt am Ende der Sammlung. Wir können die Layout-Entitäten rückwärts durchlaufen, um zum Anfang zurückzukehren.
    print('Traversing from last to first, elements between pages separated:')
    traverse_layout_backward(layout_enumerator, 1)
    # 2 -  In logischer Reihenfolge:
    # Beim Durchlaufen der Kindobjekte einer Entität, die sich über mehrere Seiten erstrecken,
    # Der Enumerator wird zwischen den Seiten wechseln, um alle Kind-Entitäten zu durchlaufen.
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
    # Nur Spans können Text enthalten.
    if layout_enumerator.type == aw.layout.LayoutEntityType.SPAN:
        print(f'{tabs}   Span contents: "{layout_enumerator.text}"')
    le_rect = layout_enumerator.rectangle
    print(f'{tabs}   Rectangle dimensions {le_rect.width}x{le_rect.height}, X={le_rect.x} Y={le_rect.y}')
    print(f'{tabs}   Page {layout_enumerator.page_index}')
```

### See Also

* module [aspose.words.layout](../../)
* class [LayoutEnumerator](../)

