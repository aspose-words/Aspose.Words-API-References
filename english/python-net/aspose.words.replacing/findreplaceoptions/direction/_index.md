---
title: FindReplaceOptions.direction property
linktitle: direction property
articleTitle: direction property
second_title: Aspose.Words for Python
description: "FindReplaceOptions.direction property. Selects direction for replace"
type: docs
weight: 40
url: /python-net/aspose.words.replacing/findreplaceoptions/direction/
---

## FindReplaceOptions.direction property

Selects direction for replace. Default value is [FindReplaceDirection.FORWARD](../../findreplacedirection/#FORWARD).



```python
@property
def direction(self) -> aspose.words.replacing.FindReplaceDirection:
    ...

@direction.setter
def direction(self, value: aspose.words.replacing.FindReplaceDirection):
    ...

```

### Examples

Shows how to determine which direction a find-and-replace operation traverses the document in (TextReplacementRecorder).

```python
class TextReplacementRecorder(aw.replacing.IReplacingCallback):

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

