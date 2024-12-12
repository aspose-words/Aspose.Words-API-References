---
title: SummaryLength enumeration
linktitle: SummaryLength enumeration
articleTitle: SummaryLength enumeration
second_title: Aspose.Words for Python
description: "aspose.words.ai.SummaryLength enumeration. Enumerates possible lengths of summary."
type: docs
weight: 80
url: /python-net/aspose.words.ai/summarylength/
---

## SummaryLength enumeration

Enumerates possible lengths of summary.


### Members

| Name | Description |
| --- | --- |
| VERY_SHORT | Try to generate 1-2 sentences. |
| SHORT | Try to generate 3-4 sentences. |
| MEDIUM | Try to generate 5-6 sentences. |
| LONG | Try to generate 7-10 sentences. |
| VERY_LONG | Try to generate 11-20 sentences. |

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

