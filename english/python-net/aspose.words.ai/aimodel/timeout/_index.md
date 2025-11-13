---
title: AiModel.timeout property
linktitle: timeout property
articleTitle: timeout property
second_title: Aspose.Words for Python
description: "AiModel.timeout property. Gets or sets the number of milliseconds to wait before the request to AI model times out"
type: docs
weight: 10
url: /python-net/aspose.words.ai/aimodel/timeout/
---

## AiModel.timeout property

Gets or sets the number of milliseconds to wait before the request to AI model times out.
The default value is 100,000 milliseconds (100 seconds).


```python
@property
def timeout(self) -> int:
    ...

@timeout.setter
def timeout(self, value: int):
    ...

```

### Examples

Shows how to change model default timeout.

```python
api_key = system_helper.environment.Environment.get_environment_variable('API_KEY')
model = aw.ai.AiModel.create(aw.ai.AiModelType.GPT_4O_MINI).with_api_key(api_key)
# Default value 100000ms.
model.timeout = 250000
```

### See Also

* module [aspose.words.ai](../../)
* class [AiModel](../)

