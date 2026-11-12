---
title: Document.show_spelling_errors property
linktitle: show_spelling_errors property
articleTitle: show_spelling_errors property
second_title: Aspose.Words for Python
description: "Document.show_spelling_errors property. Specifies whether to display spelling errors in this document."
type: docs
weight: 430
url: /tr/python-net/aspose.words/document/show_spelling_errors/
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
# Hataları yakalanacak iki cümle ekleyin
# Microsoft Word'deki yazım ve dilbilgisi denetleyicileri tarafından.
builder.writeln('There is a speling error in this sentence.')
builder.writeln('Their is a grammatical error in this sentence.')
# Bu seçenekler etkinleştirilirse, yazım hataları altı çizili olacaktır
# çıkış belgesinde kırmızı dalgalı bir çizgiyle ve dilbilgisi hatalarını çift mavi bir çizgiyle vurgular.
doc.show_grammatical_errors = show_errors
doc.show_spelling_errors = show_errors
doc.save(file_name=ARTIFACTS_DIR + 'Document.SpellingAndGrammarErrors.docx')
```

### See Also

* module [aspose.words](../../)
* class [Document](../)

