---
title: FindReplaceDirection enumeration
linktitle: FindReplaceDirection enumeration
articleTitle: FindReplaceDirection enumeration
second_title: Aspose.Words for Python
description: "aspose.words.replacing.FindReplaceDirection enumeration. Specifies direction for replace operations."
type: docs
weight: 10
url: /python-net/aspose.words.replacing/findreplacedirection/
---

## FindReplaceDirection enumeration

Specifies direction for replace operations.


### Members

| Name | Description |
| --- | --- |
| FORWARD | Matched items are replaced from first to last. |
| BACKWARD | Matched items are replaced from last back to first. |

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

* module [aspose.words.replacing](../)

