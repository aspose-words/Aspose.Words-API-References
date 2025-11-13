---
title: AiModel.translate method
linktitle: translate method
articleTitle: translate method
second_title: Aspose.Words for Python
description: "AiModel.translate method. Translates the provided document into the specified target language"
type: docs
weight: 90
url: /python-net/aspose.words.ai/aimodel/translate/
---

## translate(source_document, target_language) {#document_language}

Translates the provided document into the specified target language.
This operation leverages the connected AI model for content translating.


```python
def translate(self, source_document: aspose.words.Document, target_language: aspose.words.ai.Language):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| source_document | [Document](../../../aspose.words/document/) | The document to be translated. |
| target_language | [Language](../../language/) | The language into which the document will be translated. |

### Returns

A new [Document](../../../aspose.words/document/) object containing the translated document.


### Examples

Shows how to translate text using Google models.

```python
doc = aw.Document(file_name=MY_DIR + 'Document.docx')
api_key = system_helper.environment.Environment.get_environment_variable('API_KEY')
# Use Google generative language models.
model = aw.ai.AiModel.create(aw.ai.AiModelType.GEMINI_15_FLASH).with_api_key(api_key)
translated_doc = model.translate(doc, aw.ai.Language.ARABIC)
translated_doc.save(file_name=ARTIFACTS_DIR + 'AI.AiTranslate.docx')
```

### See Also

* module [aspose.words.ai](../../)
* class [AiModel](../)

