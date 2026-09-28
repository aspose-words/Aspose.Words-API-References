---
title: DocumentBuilder.insert_footnote method
linktitle: insert_footnote method
articleTitle: insert_footnote method
second_title: Aspose.Words for Python
description: "aspose.words.DocumentBuilder.insert_footnote method"
type: docs
weight: 340
url: /de/python-net/aspose.words/documentbuilder/insert_footnote/
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
# Fügen Sie etwas Text ein und markieren Sie ihn mit einer Fußnote, bei der die IsAuto-Eigenschaft standardmäßig auf "true" gesetzt ist,
# sodass das im Fließtext sichtbare Markierungszeichen automatisch auf "1" nummeriert wird,
# und die Fußnote am unteren Rand der Seite erscheint.
builder.write('This text will be referenced by a footnote.')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote comment regarding referenced text.')
# Fügen Sie mehr Text ein und markieren Sie ihn mit einer Endnote mit einem benutzerdefinierten Referenzzeichen,
# das anstelle der Nummer "2" verwendet wird und "IsAuto" auf false setzt.
builder.write('This text will be referenced by an endnote.')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote comment regarding referenced text.', reference_mark='CustomMark')
# Fußnoten erscheinen immer am unteren Rand des referenzierten Textes,
# sodass dieser Seitenumbruch die Fußnote nicht beeinflusst.
# Andererseits befinden sich Endnoten immer am Ende des Dokuments
# sodass dieser Seitenumbruch die Endnote auf die nächste Seite verschiebt.
builder.insert_break(aw.BreakType.PAGE_BREAK)
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.InsertFootnote.docx')
```

## See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

