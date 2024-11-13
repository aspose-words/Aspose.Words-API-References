---
title: SummaryLength enumeration
linktitle: SummaryLength enumeration
articleTitle: SummaryLength enumeration
second_title: Aspose.Words for Python
description: "aspose.words.ai.SummaryLength enumeration. Enumerates possible lengths of summary."
type: docs
weight: 70
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
first_doc = aw.Document(MyDir + "Big document.docx")
second_doc = aw.Document(MyDir + "Document.docx")
api_key = os.getenv("API_KEY")
# Use OpenAI or Google generative language models.
model = aw.ai.AiModel.create(aw.ai.AiModelType.GPT_4O_MINI).with_api_key(api_key).as_open_ai_model()
options = aw.ai.SummarizeOptions()
options.summary_length = aw.ai.SummaryLength.SHORT
one_document_summary = model.summarize(first_doc, options)
oneDocumentSummary.save(ArtifactsDir + "AI.AiSummarize.One.docx")
options.summary_length = aw.ai.SummaryLength.LONG
multi_document_summary = model.summarize([first_doc, second_doc], options)
multiDocumentSummary.save(ArtifactsDir + "AI.AiSummarize.Multi.docx")
```

### See Also

* module [aspose.words.ai](../)

