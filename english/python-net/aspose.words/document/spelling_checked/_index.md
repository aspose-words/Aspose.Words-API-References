---
title: spelling_checked property
second_title: Aspose.Words for Python via .NET API Reference
description: "Returns ``True`` if the document has been checked for spelling."
type: docs
weight: 410
url: /python-net/aspose.words/document/spelling_checked/
---

## Document.spelling_checked property

Returns ``True`` if the document has been checked for spelling.


To recheck the spelling in the document, set this property to ``False``.



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

