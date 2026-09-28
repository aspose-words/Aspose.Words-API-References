---
title: LayoutEnumerator.move_parent method
linktitle: move_parent method
articleTitle: move_parent method
second_title: Aspose.Words for Python
description: "aspose.words.layout.LayoutEnumerator.move_parent method"
type: docs
weight: 120
url: /ar/python-net/aspose.words.layout/layoutenumerator/move_parent/
---

## move_parent() {#default}

Moves to the parent entity.


```python
def move_parent(self):
    ...
```

## move_parent(types) {#layoutentitytype}

Moves to the parent entity of the specified type.


```python
def move_parent(self, types: aspose.words.layout.LayoutEntityType):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| types | [LayoutEntityType](../../layoutentitytype/) | The parent entity type to move to. Use bitwise-OR to specify multiple parent types. |

### Remarks

This method is useful if you need to find the cell, column or header/footer parent of the entity.


## Examples

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
    # يمكن فقط للـ spans أن تحتوي على نص.
    if layout_enumerator.type == aw.LayoutEntityType.SPAN:
        print(f'{tabs}   Span contents: "{layout_enumerator.text}"')
        le_rect = layout_enumerator.rectangle
        print(f'{tabs}   Rectangle dimensions {le_rect.width}x{le_rect.height}, X={le_rect.x} Y={le_rect.y}')
        print(f'{tabs}   Page {layout_enumerator.page_index}')
```

Shows ways of traversing a document's layout entities.

```python
def layout_enumerator_example():
    # افتح مستندًا يحتوي على مجموعة متنوعة من كيانات التخطيط.
    # كيانات التخطيط هي الصفحات والخلايا والصفوف والأسطر وغيرها من الكائنات المشمولة في تعداد LayoutEntityType.
    # كل كيان تخطيط يمتلك مساحة مستطيلة يشغلها في جسم المستند.
    doc = aw.Document(MY_DIR + 'Layout entities.docx')
    # أنشئ عدادًا يمكنه استعراض هذه الكيانات مثل شجرة.
    layout_enumerator = aw.layout.LayoutEnumerator(doc)
    self.assertEqual(doc, layout_enumerator.document)
    layout_enumerator.move_parent(aw.layout.LayoutEntityType.PAGE)
    self.assertEqual(aw.layout.LayoutEntityType.PAGE, layout_enumerator.type)
    with self.assertRaises(Exception):
        print(layout_enumerator.text)
    # يمكننا استدعاء هذه الطريقة للتأكد من أن العداد سيكون عند أول كيان تخطيط.
    layout_enumerator.reset()
    # هناك ترتيبان يحددان كيفية استمرار عداد التخطيط في استعراض كيانات التخطيط
    # عند مواجهته كيانات تمتد عبر صفحات متعددة.
    # 1 -  في الترتيب البصري:
    # عند الانتقال عبر عناصر الطفل للكيان التي تمتد عبر صفحات متعددة،
    # يأخذ تخطيط الصفحة الأولوية، وننتقل إلى عناصر الطفل الأخرى في هذه الصفحة ونتجنب تلك الموجودة في الصفحة التالية.
    print('Traversing from first to last, elements between pages separated:')
    traverse_layout_forward(layout_enumerator, 1)
    # المُعدِّد الخاص بنا الآن في نهاية المجموعة. يمكننا استعراض كيانات التخطيط إلى الوراء للعودة إلى البداية.
    print('Traversing from last to first, elements between pages separated:')
    traverse_layout_backward(layout_enumerator, 1)
    # 2 -  في الترتيب المنطقي:
    # عند الانتقال عبر عناصر الطفل للكيان التي تمتد عبر صفحات متعددة،
    # سيتنقل المُعدِّد بين الصفحات لاستعراض جميع كيانات الطفل.
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
    # يمكن فقط للـ spans أن تحتوي على نص.
    if layout_enumerator.type == aw.layout.LayoutEntityType.SPAN:
        print(f'{tabs}   Span contents: "{layout_enumerator.text}"')
    le_rect = layout_enumerator.rectangle
    print(f'{tabs}   Rectangle dimensions {le_rect.width}x{le_rect.height}, X={le_rect.x} Y={le_rect.y}')
    print(f'{tabs}   Page {layout_enumerator.page_index}')
```

## See Also

* module [aspose.words.layout](../../)
* class [LayoutEnumerator](../)

