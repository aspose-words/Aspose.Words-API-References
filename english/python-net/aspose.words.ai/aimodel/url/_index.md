---
title: AiModel.url property
linktitle: url property
articleTitle: url property
second_title: Aspose.Words for Python
description: "AiModel.url property. Gets or sets a URL of the model"
type: docs
weight: 20
url: /python-net/aspose.words.ai/aimodel/url/
---

## AiModel.url property

Gets or sets a URL of the model.
The default value is specific for the model.


```python
@property
def url(self) -> str:
    ...

@url.setter
def url(self, value: str):
    ...

```

### Examples

Shows how to check the grammar of a document.

```python
doc = aw.Document(file_name=MY_DIR + 'Big document.docx')
api_key = system_helper.environment.Environment.get_environment_variable('API_KEY')
# Use OpenAI generative language models.
model = aw.ai.AiModel.create(aw.ai.AiModelType.GPT_4O_MINI).with_api_key(api_key)
grammar_options = aw.ai.CheckGrammarOptions()
grammar_options.improve_stylistics = True
proofed_doc = model.check_grammar(doc, grammar_options)
proofed_doc.save(file_name=ARTIFACTS_DIR + 'AI.AiGrammar.docx')
```

Shows how to change model default url.

```python
api_key = system_helper.environment.Environment.get_environment_variable('API_KEY')
model = aw.ai.AiModel.create(aw.ai.AiModelType.GPT_4O_MINI).with_api_key(api_key)
# Default value "https:#api.openai.com/".
model.url = 'https://my.a.com/'
```

### See Also

* module [aspose.words.ai](../../)
* class [AiModel](../)

