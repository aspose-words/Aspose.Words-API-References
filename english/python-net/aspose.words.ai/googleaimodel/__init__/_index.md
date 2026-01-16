---
title: GoogleAiModel constructor
linktitle: GoogleAiModel constructor
articleTitle: GoogleAiModel constructor
second_title: Aspose.Words for Python
description: "aspose.words.ai.GoogleAiModel constructor"
type: docs
weight: 10
url: /python-net/aspose.words.ai/googleaimodel/__init__/
---

## GoogleAiModel(name) {#str}

Initializes a new instance of [GoogleAiModel](../) class.



```python
def __init__(self, name: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| name | str | The name of the model. For example, gemini-2.5-flash. |

## GoogleAiModel(name, api_key) {#str_str}

Initializes a new instance of [GoogleAiModel](../) class.



```python
def __init__(self, name: str, api_key: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| name | str | The name of the model. For example, gemini-2.5-flash. |
| api_key | str | The API key to use the Gemini API. Please refer to https://ai.google.dev/gemini-api/docs/api-key for details. |

## Examples

Shows how to use google AI model.

```python
api_key = system_helper.environment.Environment.get_environment_variable('API_KEY')
model = aw.ai.GoogleAiModel(name='gemini-flash-latest', api_key=api_key)
doc = aw.Document(file_name=MY_DIR + 'Big document.docx')
summarize_options = aw.ai.SummarizeOptions()
summarize_options.summary_length = aw.ai.SummaryLength.VERY_SHORT
summary = model.summarize(doc=doc, options=summarize_options)
```

## See Also

* module [aspose.words.ai](../../)
* class [GoogleAiModel](../)

