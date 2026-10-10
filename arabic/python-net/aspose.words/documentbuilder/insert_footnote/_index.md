---
title: DocumentBuilder.insert_footnote method
linktitle: insert_footnote method
articleTitle: insert_footnote method
second_title: Aspose.Words for Python
description: "aspose.words.DocumentBuilder.insert_footnote method"
type: docs
weight: 340
url: /ar/python-net/aspose.words/documentbuilder/insert_footnote/
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
# أدخل بعض النصوص وضع علامة عليها بحاشية مع ضبط الخاصية IsAuto على "true" افتراضيًا،
# بحيث يتم ترقيم العلامة التي تُرى في النص الأساسي تلقائيًا كـ "1",
# وستظهر الحاشية في أسفل الصفحة.
builder.write('This text will be referenced by a footnote.')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote comment regarding referenced text.')
# أدخل نصًا إضافيًا وضع علامة عليه بحاشية ختامية مع علامة مرجعية مخصصة،
# والتي ستُستبدل بالرقم "2" وتضبط "IsAuto" على false.
builder.write('This text will be referenced by an endnote.')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote comment regarding referenced text.', reference_mark='CustomMark')
# تظهر الحواشي دائمًا في أسفل النص المرجعي لها،
# لذا فإن فاصل الصفحة هذا لن يؤثر على الحاشية.
# من ناحية أخرى، الحواشي الختامية تكون دائمًا في نهاية المستند
# بحيث يدفع هذا الفاصل الحاشية الختامية إلى الصفحة التالية.
builder.insert_break(aw.BreakType.PAGE_BREAK)
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.InsertFootnote.docx')
```

## See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

