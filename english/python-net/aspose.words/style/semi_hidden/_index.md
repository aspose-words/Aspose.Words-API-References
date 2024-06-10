---
title: Style.semi_hidden property
linktitle: semi_hidden property
articleTitle: semi_hidden property
second_title: Aspose.Words for Python
description: "Style.semi_hidden property. Gets/sets whether the style hides from the Styles gallery and from the Styles task pane."
type: docs
weight: 170
url: /python-net/aspose.words/style/semi_hidden/
---

## Style.semi_hidden property

Gets/sets whether the style hides from the Styles gallery and from the Styles task pane.


```python
@property
def semi_hidden(self) -> bool:
    ...

@semi_hidden.setter
def semi_hidden(self, value: bool):
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

