---
title: AsposeLlmModel.translate method
linktitle: translate method
articleTitle: translate method
second_title: Aspose.Words for Python
description: "AsposeLlmModel.translate method. Translates the provided document into the specified target language."
type: docs
weight: 40
url: /python-net/aspose.words.ai/asposellmmodel/translate/
---

## translate(source_document, target_language) {#document_language}

Translates the provided document into the specified target language.


```python
def translate(self, source_document: aspose.words.Document, target_language: aspose.words.ai.Language):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| source_document | [Document](../../../aspose.words/document/) |  |
| target_language | [Language](../../language/) |  |

### Remarks

Same approach as [OpenAiModel.translate()](../../openaimodel/translate/#document_language): the whole document is sent as one piece of text
marked with run separators, to preserve the original formatting by restoring the translation back into
the original runs. A small local model damages a run separator more often than a cloud model, so any
run that could not be restored this way is translated again individually, by Aspose.Words.AI.AsposeLlmModel.Translate(Aspose.Words.Run,Aspose.Words.AI.Language).



### Examples

Shows how to translate a document with a local model.

```python
doc = aw.Document(file_name=MY_DIR + "Document.docx")
with aw.ai.AsposeLlmModel("Qwen25_3BPresetCpu") as model:
    translated_doc = model.translate(doc, aw.ai.Language.GERMAN)
    translated_doc.save(file_name=ARTIFACTS_DIR + "AI.AsposeLlmTranslate.docx")
```

### See Also

* module [aspose.words.ai](../../)
* class [AsposeLlmModel](../)

