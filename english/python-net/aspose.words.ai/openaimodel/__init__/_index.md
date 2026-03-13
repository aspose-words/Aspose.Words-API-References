---
title: OpenAiModel constructor
linktitle: OpenAiModel constructor
articleTitle: OpenAiModel constructor
second_title: Aspose.Words for Python
description: "aspose.words.ai.OpenAiModel constructor"
type: docs
weight: 10
url: /python-net/aspose.words.ai/openaimodel/__init__/
---

## OpenAiModel(name, api_key) {#str_str}

Initializes a new instance of [OpenAiModel](../) class.



```python
def __init__(self, name: str, api_key: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| name | str | The name of the model. For example, gpt-5.2-chat-latest. |
| api_key | str | The API key to use the OpenAi API. |

## OpenAiModel(name) {#str}

Initializes a new instance of [OpenAiModel](../) class.



```python
def __init__(self, name: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| name | str | The name of the model. For example, gpt-5.2-chat-latest. |

## Examples

Shows how to create an OpenAI model instance directly using an API key and model name.

```python
api_key = system_helper.environment.Environment.get_environment_variable("API_KEY")
# Create an OpenAI model instance using the constructor with model name and API key.
model = aw.ai.OpenAiModel(name="gpt-4o-mini", api_key=api_key)
doc = aw.Document(file_name=MY_DIR + "Big document.docx")
# Summarize the document using the OpenAI model with short summary length.
summarize_options = aw.ai.SummarizeOptions()
summarize_options.summary_length = aw.ai.SummaryLength.VERY_SHORT
summary = model.summarize(source_document=doc, options=summarize_options)
summary.save(file_name=ARTIFACTS_DIR + "OpenAiModel.OpenAiModelConstructor.docx")
```

## See Also

* module [aspose.words.ai](../../)
* class [OpenAiModel](../)

