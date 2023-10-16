---
title: DocumentBuilder.insert_footnote method
linktitle: insert_footnote method
articleTitle: insert_footnote method
second_title: Aspose.Words for Python
description: "aspose.words.DocumentBuilder.insert_footnote method"
type: docs
weight: 340
url: /python-net/aspose.words/documentbuilder/insert_footnote/
---

## insert_footnote(footnote_type, footnote_text) {#footnotetype_str}

Inserts a footnote or endnote into the document.


```python
def insert_footnote(self, footnote_type: aspose.words.notes.FootnoteType, footnote_text: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| footnote_type | [FootnoteType](../../../aspose.words.notes/footnotetype/) |  |
| footnote_text | str |  |

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
| footnote_type | [FootnoteType](../../../aspose.words.notes/footnotetype/) |  |
| footnote_text | str |  |
| reference_mark | str |  |

### Returns

Returns a footnote object that was just created.


## Examples

Shows how to reference text with a footnote and an endnote.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Insert some text and mark it with a footnote with the "is_auto" property set to "True" by default,
# so the marker seen in the body text will be auto-numbered at "1",
# and the footnote will appear at the bottom of the page.
builder.write("This text will be referenced by a footnote.")
builder.insert_footnote(aw.notes.FootnoteType.FOOTNOTE, "Footnote comment regarding referenced text.")

# Insert more text and mark it with an endnote with a custom reference mark,
# which will be used in place of the number "2" and set "is_auto" to False.
builder.write("This text will be referenced by an endnote.")
builder.insert_footnote(aw.notes.FootnoteType.ENDNOTE, "Endnote comment regarding referenced text.", "CustomMark")

# Footnotes always appear at the bottom of their referenced text,
# so this page break will not affect the footnote.
# On the other hand, endnotes are always at the end of the document
# so that this page break will push the endnote down to the next page.
builder.insert_break(aw.BreakType.PAGE_BREAK)

doc.save(ARTIFACTS_DIR + "DocumentBuilder.insert_footnote.docx")
```

## See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

