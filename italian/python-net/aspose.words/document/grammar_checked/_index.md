---
title: Document.grammar_checked property
linktitle: grammar_checked property
articleTitle: grammar_checked property
second_title: Aspose.Words for Python
description: "Document.grammar_checked property. Returns ``True`` if the document has been checked for grammar."
type: docs
weight: 190
url: /it/python-net/aspose.words/document/grammar_checked/
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
# La stringa con errori ortografici.
doc.first_section.body.first_paragraph.runs.add(aw.Run(doc=doc, text='The speeling in this documentz is all broked.'))
# Il controllo ortografia/grammatica inizia se impostiamo le proprietà su false.
# Possiamo vedere tutti gli errori in Microsoft Word tramite Revisione -> Ortografia e grammatica.
# Nota che Microsoft Word non avvia automaticamente il controllo grammaticale/ortografico per i formati di documento DOC e RTF.
doc.spelling_checked = check_spelling_grammar
doc.grammar_checked = check_spelling_grammar
doc.save(file_name=ARTIFACTS_DIR + 'Document.SpellingOrGrammar.docx')
```

### See Also

* module [aspose.words](../../)
* class [Document](../)

