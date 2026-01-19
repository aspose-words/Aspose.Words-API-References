---
title: CheckGrammarOptions.preserve_formatting property
linktitle: preserve_formatting property
articleTitle: preserve_formatting property
second_title: Aspose.Words for Python
description: "CheckGrammarOptions.preserve_formatting property. Allows to specify either [AiModel.check_grammar()](../../aimodel/check_grammar/#document_checkgrammaroptions) will try to preserve layout and formatting of the original document, or not"
type: docs
weight: 40
url: /python-net/aspose.words.ai/checkgrammaroptions/preserve_formatting/
---

## CheckGrammarOptions.preserve_formatting property

Allows to specify either [AiModel.check_grammar()](../../aimodel/check_grammar/#document_checkgrammaroptions) will try to preserve
layout and formatting of the original document, or not.
Default value is ``True``.



```python
@property
def preserve_formatting(self) -> bool:
    ...

@preserve_formatting.setter
def preserve_formatting(self, value: bool):
    ...

```

### Remarks

When the option is set to ``False``, the quality of grammar checking is higher
than when this option is set to ``True``. However, the original formatting of the
text is not preserved in this case.



### See Also

* module [aspose.words.ai](../../)
* class [CheckGrammarOptions](../)

