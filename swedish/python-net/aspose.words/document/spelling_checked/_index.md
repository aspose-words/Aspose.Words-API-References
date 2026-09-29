---
title: Document.spelling_checked property
linktitle: spelling_checked property
articleTitle: spelling_checked property
second_title: Aspose.Words for Python
description: "Document.spelling_checked property. Returns ``True`` if the document has been checked for spelling."
type: docs
weight: 440
url: /sv/python-net/aspose.words/document/spelling_checked/
---

## Document.spelling_checked property

Returns ``True`` if the document has been checked for spelling.



```python
@property
def spelling_checked(self) -> bool:
    ...

@spelling_checked.setter
def spelling_checked(self, value: bool):
    ...

```

### Remarks

To recheck the spelling in the document, set this property to ``False``.



### Examples

Shows how to set spelling or grammar verifying.

```python
doc = aw.Document()
# Strängen med stavfel.
doc.first_section.body.first_paragraph.runs.add(aw.Run(doc=doc, text='The speeling in this documentz is all broked.'))
# Stavnings-/grammatikgranskning startar om vi sätter egenskaperna till falskt.
# Vi kan se alla fel i Microsoft Word via Granska -> Stavning & Grammatik.
# Observera att Microsoft Word inte startar grammatik-/stavningskontroll automatiskt för DOC- och RTF-dokumentformat.
doc.spelling_checked = check_spelling_grammar
doc.grammar_checked = check_spelling_grammar
doc.save(file_name=ARTIFACTS_DIR + 'Document.SpellingOrGrammar.docx')
```

### See Also

* module [aspose.words](../../)
* class [Document](../)

