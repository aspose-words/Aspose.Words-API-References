---
title: Style.unhide_when_used property
linktitle: unhide_when_used property
articleTitle: unhide_when_used property
second_title: Aspose.Words for Python
description: "Style.unhide_when_used property. Gets/sets whether the style used in the current document unhides from the Styles gallery and from the Styles task pane"
type: docs
weight: 210
url: /python-net/aspose.words/style/unhide_when_used/
---

## Style.unhide_when_used property

Gets/sets whether the style used in the current document unhides from the Styles gallery and from the Styles task pane.
True when the used style should be shown in the Styles gallery.


```python
@property
def unhide_when_used(self) -> bool:
    ...

@unhide_when_used.setter
def unhide_when_used(self, value: bool):
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

doc.save(file_name=ARTIFACTS_DIR + "Styles.StylePriority.docx")
```

### See Also

* module [aspose.words](../../)
* class [Style](../)

