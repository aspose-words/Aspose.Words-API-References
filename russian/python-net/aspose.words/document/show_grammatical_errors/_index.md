---
title: Document.show_grammatical_errors property
linktitle: show_grammatical_errors property
articleTitle: show_grammatical_errors property
second_title: Aspose.Words for Python
description: "Document.show_grammatical_errors property. Specifies whether to display grammar errors in this document."
type: docs
weight: 420
url: /ru/python-net/aspose.words/document/show_grammatical_errors/
---

## Document.show_grammatical_errors property

Specifies whether to display grammar errors in this document.


```python
@property
def show_grammatical_errors(self) -> bool:
    ...

@show_grammatical_errors.setter
def show_grammatical_errors(self, value: bool):
    ...

```

### Examples

Shows how to show/hide errors in the document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Вставьте два предложения с ошибками, которые будут обнаружены
# проверяющими правописание и грамматику в Microsoft Word.
builder.writeln('There is a speling error in this sentence.')
builder.writeln('Their is a grammatical error in this sentence.')
# Если эти параметры включены, то орфографические ошибки будут подчёркнуты
# в выходном документе зубчатой красной линией, а двойная синяя линия будет выделять грамматические ошибки.
doc.show_grammatical_errors = show_errors
doc.show_spelling_errors = show_errors
doc.save(file_name=ARTIFACTS_DIR + 'Document.SpellingAndGrammarErrors.docx')
```

### See Also

* module [aspose.words](../../)
* class [Document](../)

