---
title: Document.grammar_checked property
linktitle: grammar_checked property
articleTitle: grammar_checked property
second_title: Aspose.Words for Python
description: "Document.grammar_checked property. Returns ``True`` if the document has been checked for grammar."
type: docs
weight: 190
url: /fr/python-net/aspose.words/document/grammar_checked/
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
# La chaîne contenant des fautes d'orthographe.
doc.first_section.body.first_paragraph.runs.add(aw.Run(doc=doc, text='The speeling in this documentz is all broked.'))
# La vérification orthographique/grammaticale démarre si nous définissons les propriétés sur false.
# Nous pouvons voir toutes les erreurs dans Microsoft Word via Révision -> Orthographe et Grammaire.
# Notez que Microsoft Word ne lance pas automatiquement la vérification grammaticale/orthographique pour les formats de document DOC et RTF.
doc.spelling_checked = check_spelling_grammar
doc.grammar_checked = check_spelling_grammar
doc.save(file_name=ARTIFACTS_DIR + 'Document.SpellingOrGrammar.docx')
```

### See Also

* module [aspose.words](../../)
* class [Document](../)

