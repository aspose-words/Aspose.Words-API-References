---
title: FindReplaceOptions.use_legacy_order property
linktitle: use_legacy_order property
articleTitle: use_legacy_order property
second_title: Aspose.Words for Python
description: "FindReplaceOptions.use_legacy_order property. True indicates that a text search is performed sequentially from top to bottom considering the text boxes"
type: docs
weight: 190
url: /python-net/aspose.words.replacing/findreplaceoptions/use_legacy_order/
---

## FindReplaceOptions.use_legacy_order property

True indicates that a text search is performed sequentially from top to bottom considering the text boxes.
Default value is ``False``.



```python
@property
def use_legacy_order(self) -> bool:
    ...

@use_legacy_order.setter
def use_legacy_order(self, value: bool):
    ...

```

### Examples

Shows how to change the searching order of nodes when performing a find-and-replace text operation (TextReplacementTracker).

```python
class TextReplacementTracker(aw.replacing.IReplacingCallback):

    @property
    def matches(self):
        pass

    def replacing(self, e):
        matches.append(e.match.value)
        return aw.replacing.ReplaceAction.REPLACE
```

### See Also

* module [aspose.words.replacing](../../)
* class [FindReplaceOptions](../)

