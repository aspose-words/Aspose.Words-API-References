---
title: Style.priority property
linktitle: priority property
articleTitle: priority property
second_title: Aspose.Words for Python
description: "Style.priority property. Gets/sets the integer value that represents the priority for sorting the styles in the Styles task pane."
type: docs
weight: 160
url: /python-net/aspose.words/style/priority/
---

## Style.priority property

Gets/sets the integer value that represents the priority for sorting the styles in the Styles task pane.


```python
@property
def priority(self) -> int:
    ...

@priority.setter
def priority(self, value: int):
    ...

```

### Examples

Shows how to prioritize and hide a style.

```python
doc = aw.Document()
style_title = doc.styles.get_by_style_identifier(aw.StyleIdentifier.SUBTITLE)
if style_title.priority == 9:
    style_title.priority = 10
if not style_title.unhide_when_used:
    style_title.unhide_when_used = True
if style_title.semi_hidden:
    style_title.semi_hidden = True
doc.save(file_name=ARTIFACTS_DIR + 'Styles.StylePriority.docx')
```

### See Also

* module [aspose.words](../../)
* class [Style](../)

