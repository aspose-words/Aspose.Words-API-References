---
title: LayoutEnumerator class
linktitle: LayoutEnumerator class
articleTitle: LayoutEnumerator class
second_title: Aspose.Words for Python
description: "aspose.words.layout.LayoutEnumerator class. Enumerates page layout entities of a document."
type: docs
weight: 60
url: /ru/python-net/aspose.words.layout/layoutenumerator/
---

## LayoutEnumerator class

Enumerates page layout entities of a document.

You can use this class to walk over the page layout model. Available properties are type, geometry, text and page index where entity is rendered,
as well as overall structure and relationships.
Use combination of Aspose.Words.Layout.LayoutCollector.GetEntity(Aspose.Words.Node) and Aspose.Words.Layout.LayoutEnumerator.Current move to the entity which corresponds to a document node.
To learn more, visit the [Converting to Fixed-page Format](https://docs.aspose.com/words/python-net/converting-to-fixed-page-format/) documentation article.




### Constructors
| Name | Description |
| --- | --- |
| [LayoutEnumerator(document)](./__init__/#document) | Initializes new instance of this class. |

### Properties

| Name | Description |
| --- | --- |
| [document](./document/) | Gets document this instance enumerates. |
| [kind](./kind/) | Gets the kind of the current entity. This can be an empty string but never ``None``. |
| [page_index](./page_index/) | Gets the 1-based index of a page which contains the current entity. |
| [rectangle](./rectangle/) | Returns the bounding rectangle of the current entity relative to the page top left corner (in points). |
| [text](./text/) | Gets text of the current span entity. Throws for other entity types. |
| [type](./type/) | Gets the type of the current entity. |

### Methods

| Name | Description |
| --- | --- |
|[ move_first_child()](./move_first_child/#default) | Moves to the first child entity. |
|[ move_last_child()](./move_last_child/#default) | Moves to the last child entity. |
|[ move_next()](./move_next/#default) | Moves to the next sibling entity in visual order. |
|[ move_next_logical()](./move_next_logical/#default) | Moves to the next sibling entity in a logical order. |
|[ move_parent()](./move_parent/#default) | Moves to the parent entity. |
|[ move_parent(types)](./move_parent/#layoutentitytype) | Moves to the parent entity of the specified type. |
|[ move_previous()](./move_previous/#default) | Moves to the previous sibling entity. |
|[ move_previous_logical()](./move_previous_logical/#default) | Moves to the previous sibling entity in a logical order. |
|[ reset()](./reset/#default) | Moves the enumerator to the first page of the document. |
|[ set_current(collector, node)](./set_current/#layoutcollector_node) | Extracts an opaque position of the [LayoutEnumerator](./) which corresponds to the specified node and sets this position as current position in the page layout model |

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
    # Только spans могут содержать текст.
    if layout_enumerator.type == aw.LayoutEntityType.SPAN:
        print(f'{tabs}   Span contents: "{layout_enumerator.text}"')
        le_rect = layout_enumerator.rectangle
        print(f'{tabs}   Rectangle dimensions {le_rect.width}x{le_rect.height}, X={le_rect.x} Y={le_rect.y}')
        print(f'{tabs}   Page {layout_enumerator.page_index}')
```

Shows ways of traversing a document's layout entities.

```python
def layout_enumerator_example():
    # Откройте документ, содержащий разнообразные элементы разметки.
    # Элементы разметки — это страницы, ячейки, строки, линии и другие объекты, включённые в перечисление LayoutEntityType.
    # Каждый элемент разметки имеет прямоугольное пространство, которое он занимает в теле документа.
    doc = aw.Document(MY_DIR + 'Layout entities.docx')
    # Создайте перечислитель, который может обходить эти элементы как дерево.
    layout_enumerator = aw.layout.LayoutEnumerator(doc)
    self.assertEqual(doc, layout_enumerator.document)
    layout_enumerator.move_parent(aw.layout.LayoutEntityType.PAGE)
    self.assertEqual(aw.layout.LayoutEntityType.PAGE, layout_enumerator.type)
    with self.assertRaises(Exception):
        print(layout_enumerator.text)
    # Мы можем вызвать этот метод, чтобы убедиться, что перечислитель находится на первом элементе разметки.
    layout_enumerator.reset()
    # Существует два порядка, определяющих, как перечислитель разметки продолжает обход элементов разметки
    # когда он встречает элементы, охватывающие несколько страниц.
    # 1 -  В визуальном порядке:
    # При перемещении по дочерним элементам сущности, охватывающим несколько страниц,
    # Макет страницы имеет приоритет, и мы переходим к другим дочерним элементам на этой странице, избегая тех, что на следующей.
    print('Traversing from first to last, elements between pages separated:')
    traverse_layout_forward(layout_enumerator, 1)
    # Наш перечислитель теперь находится в конце коллекции. Мы можем перемещаться по элементам макета назад, чтобы вернуться в начало.
    print('Traversing from last to first, elements between pages separated:')
    traverse_layout_backward(layout_enumerator, 1)
    # 2 -  В логическом порядке:
    # При перемещении по дочерним элементам сущности, охватывающим несколько страниц,
    # Перечислитель будет перемещаться между страницами, чтобы пройти все дочерние элементы.
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
    # Только spans могут содержать текст.
    if layout_enumerator.type == aw.layout.LayoutEntityType.SPAN:
        print(f'{tabs}   Span contents: "{layout_enumerator.text}"')
    le_rect = layout_enumerator.rectangle
    print(f'{tabs}   Rectangle dimensions {le_rect.width}x{le_rect.height}, X={le_rect.x} Y={le_rect.y}')
    print(f'{tabs}   Page {layout_enumerator.page_index}')
```

### See Also

* module [aspose.words.layout](../)

