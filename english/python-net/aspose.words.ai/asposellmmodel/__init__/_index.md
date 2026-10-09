---
title: AsposeLlmModel constructor
linktitle: AsposeLlmModel constructor
articleTitle: AsposeLlmModel constructor
second_title: Aspose.Words for Python
description: "AsposeLlmModel constructor. Initializes a new instance of the [AsposeLlmModel](../) class for a specified Aspose.LLM preset."
type: docs
weight: 10
url: /python-net/aspose.words.ai/asposellmmodel/__init__/
---

## AsposeLlmModel(preset_name) {#str}

Initializes a new instance of the [AsposeLlmModel](../) class for a specified Aspose.LLM preset.



```python
def __init__(self, preset_name: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| preset_name | str | The name of the Aspose.LLM preset class that selects the local model family and its runtime, for example "Qwen25Preset". Nothing is loaded or downloaded when this constructor runs. |

### Examples

Shows how to summarize documents with a local model, so the content never leaves the machine.

```python
# Aspose.LLM is a separate package with its own license, for example:
# new Aspose.LLM.License().SetLicense("Aspose.Total.lic");
first_doc = aw.Document(file_name=MY_DIR + "Big document.docx")
second_doc = aw.Document(file_name=MY_DIR + "Document.docx")
# Disposing the model releases the local model and its native resources.
with aw.ai.AsposeLlmModel("Qwen25_3BPresetCpu") as model:
    summarize_options = aw.ai.SummarizeOptions()
    summarize_options.summary_length = aw.ai.SummaryLength.SHORT
    summary = model.summarize(source_document=first_doc, options=summarize_options)
    summary.save(file_name=ARTIFACTS_DIR + "AI.AsposeLlmSummarize.One.docx")
    summarize_options.summary_length = aw.ai.SummaryLength.MEDIUM
    combined_summary = model.summarize(source_documents=[first_doc, second_doc], options=summarize_options)
    combined_summary.save(file_name=ARTIFACTS_DIR + "AI.AsposeLlmSummarize.Multiple.docx")
```

### See Also

* module [aspose.words.ai](../../)
* class [AsposeLlmModel](../)

