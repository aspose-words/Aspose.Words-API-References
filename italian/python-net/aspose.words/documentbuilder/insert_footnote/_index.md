---
title: DocumentBuilder.insert_footnote method
linktitle: insert_footnote method
articleTitle: insert_footnote method
second_title: Aspose.Words for Python
description: "aspose.words.DocumentBuilder.insert_footnote method"
type: docs
weight: 340
url: /it/python-net/aspose.words/documentbuilder/insert_footnote/
---

## insert_footnote(footnote_type, footnote_text) {#footnotetype_str}

Inserts a footnote or endnote into the document.


```python
def insert_footnote(self, footnote_type: aspose.words.notes.FootnoteType, footnote_text: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| footnote_type | [FootnoteType](../../../aspose.words.notes/footnotetype/) | Specifies whether to insert a footnote or an endnote. |
| footnote_text | str | Specifies the text of the footnote. |

### Returns

Returns a footnote object that was just created.


## insert_footnote(footnote_type, footnote_text, reference_mark) {#footnotetype_str_str}

Inserts a footnote or endnote into the document.


```python
def insert_footnote(self, footnote_type: aspose.words.notes.FootnoteType, footnote_text: str, reference_mark: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| footnote_type | [FootnoteType](../../../aspose.words.notes/footnotetype/) | Specifies whether to insert a footnote or an endnote. |
| footnote_text | str | Specifies the text of the footnote. |
| reference_mark | str | Specifies the custom reference mark of the footnote. |

### Returns

Returns a footnote object that was just created.


## Examples

Shows how to reference text with a footnote and an endnote.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Inserisci del testo e contrassegnalo con una nota a piè di pagina con la proprietà IsAuto impostata su "true" per impostazione predefinita,
# in modo che il marcatore visualizzato nel testo principale sia numerato automaticamente a "1",
# e la nota a piè di pagina apparirà in fondo alla pagina.
builder.write('This text will be referenced by a footnote.')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote comment regarding referenced text.')
# Inserisci altro testo e contrassegnalo con una nota di chiusura con un marcatore di riferimento personalizzato,
# che verrà usato al posto del numero "2" e imposterà "IsAuto" su false.
builder.write('This text will be referenced by an endnote.')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote comment regarding referenced text.', reference_mark='CustomMark')
# Le note a piè di pagina appaiono sempre in fondo al loro testo di riferimento,
# quindi questo interruzione di pagina non influenzerà la nota a piè di pagina.
# D'altra parte, le note di chiusura sono sempre alla fine del documento
# in modo che questa interruzione di pagina spinga la nota di chiusura alla pagina successiva.
builder.insert_break(aw.BreakType.PAGE_BREAK)
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.InsertFootnote.docx')
```

## See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

