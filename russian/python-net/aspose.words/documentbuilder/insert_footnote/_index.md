---
title: DocumentBuilder.insert_footnote method
linktitle: insert_footnote method
articleTitle: insert_footnote method
second_title: Aspose.Words for Python
description: "aspose.words.DocumentBuilder.insert_footnote method"
type: docs
weight: 340
url: /ru/python-net/aspose.words/documentbuilder/insert_footnote/
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
# Вставьте некоторый текст и пометьте его сноской, у которой свойство IsAuto по умолчанию установлено в "true",
# чтобы маркер, видимый в основном тексте, был автоматически пронумерован как "1",
# и сноска появится внизу страницы.
builder.write('This text will be referenced by a footnote.')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote comment regarding referenced text.')
# Вставьте ещё текст и пометьте его конечной сноской с пользовательским маркером ссылки,
# который будет использоваться вместо числа "2" и установит "IsAuto" в false.
builder.write('This text will be referenced by an endnote.')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote comment regarding referenced text.', reference_mark='CustomMark')
# Сноски всегда появляются внизу текста, к которому они относятся,
# поэтому разрыв страницы не повлияет на сноску.
# С другой стороны, конечные сноски всегда находятся в конце документа
# поэтому этот разрыв страницы переместит конечную сноску на следующую страницу.
builder.insert_break(aw.BreakType.PAGE_BREAK)
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.InsertFootnote.docx')
```

## See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

