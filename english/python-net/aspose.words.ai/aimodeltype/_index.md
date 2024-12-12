---
title: AiModelType enumeration
linktitle: AiModelType enumeration
articleTitle: AiModelType enumeration
second_title: Aspose.Words for Python
description: "aspose.words.ai.AiModelType enumeration. Represents the types of [AiModel](../aimodel/) that can be integrated into the document processing workflow."
type: docs
weight: 20
url: /python-net/aspose.words.ai/aimodeltype/
---

## AiModelType enumeration

Represents the types of [AiModel](../aimodel/) that can be integrated into the document processing workflow.


This enumeration is used to define which large language model (LLM) should be utilized for tasks
such as summarization, translation, and content generation.


### Members

| Name | Description |
| --- | --- |
| GPT_4O | GPT-4o generative model type. |
| GPT_4O_MINI | GPT-4o mini generative model type. |
| GPT_4_TURBO | GPT-4 Turbo generative model type. |
| GPT_35_TURBO | GPT-3.5 Turbo generative model type. |
| GEMINI_15_FLASH | Gemini 1.5 Flash generative model type. |
| GEMINI_15_FLASH_8B | Gemini 1.5 Flash-8B generative model type. |
| GEMINI_15_PRO | Gemini 1.5 Pro generative model type. |

### Examples

Shows how to summarize text using OpenAI and Google models.

```python
first_doc = aw.Document(file_name=MY_DIR + "Big document.docx")
second_doc = aw.Document(file_name=MY_DIR + "Document.docx")
api_key = system_helper.environment.Environment.get_environment_variable("API_KEY")
# Use OpenAI or Google generative language models.
model = aw.ai.AiModel.create(aw.ai.AiModelType.GPT_4O_MINI).with_api_key(api_key).as_open_ai_model()
options = aw.ai.SummarizeOptions()
options.summary_length = aw.ai.SummaryLength.SHORT
one_document_summary = model.summarize(source_document=first_doc, options=options)
one_document_summary.save(file_name=ARTIFACTS_DIR + "AI.AiSummarize.One.docx")
options.summary_length = aw.ai.SummaryLength.LONG
multi_document_summary = model.summarize(source_documents=[first_doc, second_doc], options=options)
multi_document_summary.save(file_name=ARTIFACTS_DIR + "AI.AiSummarize.Multi.docx")
```

### See Also

* module [aspose.words.ai](../)

