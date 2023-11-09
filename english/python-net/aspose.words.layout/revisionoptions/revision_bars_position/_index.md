---
title: RevisionOptions.revision_bars_position property
linktitle: revision_bars_position property
articleTitle: revision_bars_position property
second_title: Aspose.Words for Python
description: "RevisionOptions.revision_bars_position property. Gets or sets rendering position of revision bars"
type: docs
weight: 140
url: /python-net/aspose.words.layout/revisionoptions/revision_bars_position/
---

## RevisionOptions.revision_bars_position property

Gets or sets rendering position of revision bars.
Default value is [HorizontalAlignment.OUTSIDE](../../../aspose.words.drawing/horizontalalignment/#OUTSIDE).



```python
@property
def revision_bars_position(self) -> aspose.words.drawing.HorizontalAlignment:
    ...

@revision_bars_position.setter
def revision_bars_position(self, value: aspose.words.drawing.HorizontalAlignment):
    ...

```

### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(ArgumentOutOfRangeException)) | Values of [HorizontalAlignment.CENTER](../../../aspose.words.drawing/horizontalalignment/#CENTER) and [HorizontalAlignment.INSIDE](../../../aspose.words.drawing/horizontalalignment/#INSIDE)  are not allowed. |

### See Also

* module [aspose.words.layout](../../)
* class [RevisionOptions](../)

