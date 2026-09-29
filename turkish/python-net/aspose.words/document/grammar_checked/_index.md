---
title: Document.grammar_checked property
linktitle: grammar_checked property
articleTitle: grammar_checked property
second_title: Aspose.Words for Python
description: "Document.grammar_checked property. Returns ``True`` if the document has been checked for grammar."
type: docs
weight: 190
url: /tr/python-net/aspose.words/document/grammar_checked/
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
# Yazım hataları içeren dize.
doc.first_section.body.first_paragraph.runs.add(aw.Run(doc=doc, text='The speeling in this documentz is all broked.'))
# Özellikleri false (yanlış) olarak ayarlarsak, Yazım/Dilbilgisi denetimi başlar.
# Microsoft Word'te Review -> Spelling & Grammar aracılığıyla tüm hataları görebiliriz.
# Microsoft Word'ün DOC ve RTF belge formatları için dilbilgisi/yazım denetimini otomatik olarak başlatmadığını unutmayın.
doc.spelling_checked = check_spelling_grammar
doc.grammar_checked = check_spelling_grammar
doc.save(file_name=ARTIFACTS_DIR + 'Document.SpellingOrGrammar.docx')
```

### See Also

* module [aspose.words](../../)
* class [Document](../)

