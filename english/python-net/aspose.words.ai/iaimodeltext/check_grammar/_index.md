---
title: IAiModelText.check_grammar method
linktitle: check_grammar method
articleTitle: check_grammar method
second_title: Aspose.Words for Python
description: "IAiModelText.check_grammar method. Checks grammar of the provided document"
type: docs
weight: 10
url: /python-net/aspose.words.ai/iaimodeltext/check_grammar/
---

## check_grammar(source_document, options) {#document_checkgrammaroptions}

Checks grammar of the provided document.
This operation leverages the connected AI model for checking grammar of document.


```python
def check_grammar(self, source_document: aspose.words.Document, options: aspose.words.ai.CheckGrammarOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| source_document | [Document](../../../aspose.words/document/) | The document being checked for grammar. |
| options | [CheckGrammarOptions](../../checkgrammaroptions/) | Optional settings to control how grammar will be checked. |

### Returns

A new [Document](../../../aspose.words/document/) with checked grammar.


### Examples

Shows how to check the grammar of a document.

```python
doc = aw.Document(file_name=MY_DIR + 'Big document.docx')
api_key = system_helper.environment.Environment.get_environment_variable('API_KEY')
# Use OpenAI generative language models.
model = aw.ai.AiModel.create(aw.ai.AiModelType.GPT_4O_MINI).with_api_key(api_key).as_open_ai_model()
grammar_options = aw.ai.CheckGrammarOptions()
grammar_options.improve_stylistics = True
proofed_doc = model.check_grammar(doc, grammar_options)
proofed_doc.save(file_name=ARTIFACTS_DIR + 'AI.AiGrammar.docx')
```

### See Also

* module [aspose.words.ai](../../)
* class [IAiModelText](../)

