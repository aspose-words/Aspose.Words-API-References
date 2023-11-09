---
title: Document.grammar_checked property
linktitle: grammar_checked property
articleTitle: grammar_checked property
second_title: Aspose.Words for Python
description: "Document.grammar_checked property. Returns ``True`` if the document has been checked for grammar."
type: docs
weight: 180
url: /python-net/aspose.words/document/grammar_checked/
---

## Document.grammar_checked property

Returns ``True`` if the document has been checked for grammar.



```python
@property
def grammar_checked(self) -> bool:
    ...

@grammar_checked.setter
def grammar_checked(self, value: bool):
    ...

```

### Remarks

To recheck the grammar in the document, set this property to ``False``.



### Examples

Shows how to set spelling or grammar verifying.

```python
doc = aw.Document()

# The string with spelling errors.
doc.first_section.body.first_paragraph.runs.add(aw.Run(doc, "The speeling in this documentz is all broked."))

# Spelling/Grammar check start if we set properties to False.
# We can see all errors in Microsoft Word via Review -> Spelling & Grammar.
# Note that Microsoft Word does not start grammar/spell check automatically for DOC and RTF document format.
doc.spelling_checked = check_spelling_grammar
doc.grammar_checked = check_spelling_grammar

doc.save(ARTIFACTS_DIR + "Document.spelling_or_grammar.docx")
```

### See Also

* module [aspose.words](../../)
* class [Document](../)

