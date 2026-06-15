---
title: LoadOptions.warning_callback property
linktitle: warning_callback property
articleTitle: warning_callback property
second_title: Aspose.Words for Python
description: "LoadOptions.warning_callback property. Called during a load operation, when an issue is detected that might result in data or formatting fidelity loss."
type: docs
weight: 190
url: /python-net/aspose.words.loading/loadoptions/warning_callback/
---

## LoadOptions.warning_callback property

Called during a load operation, when an issue is detected that might result in data or formatting fidelity loss.


```python
@property
def warning_callback(self) -> aspose.words.IWarningCallback:
    ...

@warning_callback.setter
def warning_callback(self, value: aspose.words.IWarningCallback):
    ...

```

### Examples

Shows how to print and store warnings that occur during document loading (DocumentLoadingWarningCallback).

```python
class DocumentLoadingWarningCallback(aw.IWarningCallback):

    def __init__(self):
        self.m_warnings = []

    def warning(self, info):
        print(f'Warning: {info.warning_type}')
        print(f'\tSource: {info.source}')
        print(f'\tDescription: {info.description}')
        self.m_warnings.append(info)

    def get_warnings(self):
        return self.m_warnings
```

### See Also

* module [aspose.words.loading](../../)
* class [LoadOptions](../)

