---
title: Document.show_spelling_errors property
linktitle: show_spelling_errors property
articleTitle: show_spelling_errors property
second_title: Aspose.Words for Python
description: "Document.show_spelling_errors property. Specifies whether to display spelling errors in this document."
type: docs
weight: 420
url: /python-net/aspose.words/document/show_spelling_errors/
---

## Document.show_spelling_errors property

Specifies whether to display spelling errors in this document.


```python
@property
def show_spelling_errors(self) -> bool:
    ...

@show_spelling_errors.setter
def show_spelling_errors(self, value: bool):
    ...

```

### Examples

Shows how to show/hide errors in the document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Insert two sentences with mistakes that would be picked up
# by the spelling and grammar checkers in Microsoft Word.
builder.writeln('There is a speling error in this sentence.')
builder.writeln('Their is a grammatical error in this sentence.')
# If these options are enabled, then spelling errors will be underlined
# in the output document by a jagged red line, and a double blue line will highlight grammatical mistakes.
doc.show_grammatical_errors = show_errors
doc.show_spelling_errors = show_errors
doc.save(file_name=ARTIFACTS_DIR + 'Document.SpellingAndGrammarErrors.docx')
```

### See Also

* module [aspose.words](../../)
* class [Document](../)

