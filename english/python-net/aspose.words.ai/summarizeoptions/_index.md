---
title: SummarizeOptions class
linktitle: SummarizeOptions class
articleTitle: SummarizeOptions class
second_title: Aspose.Words for Python
description: "aspose.words.ai.SummarizeOptions class. Allows to specify various options for summarizing document content."
type: docs
weight: 60
url: /python-net/aspose.words.ai/summarizeoptions/
---

## SummarizeOptions class

Allows to specify various options for summarizing document content.


### Constructors
| Name | Description |
| --- | --- |
| [SummarizeOptions()](./__init__/#default) | Initializes a new instances of [SummarizeOptions](./) class. |

### Properties

| Name | Description |
| --- | --- |
| [summary_length](./summary_length/) | Allows to specify summary length. Default value is [SummaryLength.MEDIUM](../summarylength/#MEDIUM). |

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

