---
title: CheckGrammarOptions class
linktitle: CheckGrammarOptions class
articleTitle: CheckGrammarOptions class
second_title: Aspose.Words for Python
description: "aspose.words.ai.CheckGrammarOptions class. Allows to specify various options while checking grammar of a document using AI."
type: docs
weight: 40
url: /python-net/aspose.words.ai/checkgrammaroptions/
---

## CheckGrammarOptions class

Allows to specify various options while checking grammar of a document using AI.


### Constructors
| Name | Description |
| --- | --- |
| [CheckGrammarOptions()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [improve_stylistics](./improve_stylistics/) | Allows to specify either AI will try to improve stylistics of the text being proofed. Default value is ``False``. |
| [make_revisions](./make_revisions/) | Allows to specify either final or revised document to be returned with proofed text. Default value is ``False``. |
| [preserve_formatting](./preserve_formatting/) | Allows to specify either [IAiModelText.check_grammar()](../iaimodeltext/check_grammar/#document_checkgrammaroptions) will try to preserve layout and formatting of the original document, or not. Default value is ``True``. |

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

### See Also

* module [aspose.words.ai](../)

