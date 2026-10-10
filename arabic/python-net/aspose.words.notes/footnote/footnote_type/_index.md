---
title: Footnote.footnote_type property
linktitle: footnote_type property
articleTitle: footnote_type property
second_title: Aspose.Words for Python
description: "Footnote.footnote_type property. Returns a value that specifies whether this is a footnote or endnote."
type: docs
weight: 30
url: /ar/python-net/aspose.words.notes/footnote/footnote_type/
---

## Footnote.footnote_type property

Returns a value that specifies whether this is a footnote or endnote.


```python
@property
def footnote_type(self) -> aspose.words.notes.FootnoteType:
    ...

```

### Examples

Shows the difference between footnotes and endnotes.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# فيما يلي طريقتان لإرفاق مراجع مرقمة بالنص. كلا هذين المرجعين سيضيفان a
# علامة مرجعية صغيرة مرتفعة في الموقع الذي ندرجها فيه.
# علامة المرجعية، بشكل افتراضي، هي رقم الفهرس للمرجعية بين جميع المراجع في المستند.
# كل مرجعية ستنشئ أيضًا إدخالًا، سيكون له نفس علامة المرجعية كما في نص الجسم.
# ونص المرجعية، الذي سنمرره إلى طريقة "InsertFootnote" الخاصة بمنشئ المستند.
# 1 -  حاشية سفلية، سيظهر إدخالها في نفس الصفحة مع النص الذي تشير إليه:
builder.write('Footnote referenced main body text.')
footnote = builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote text, will appear at the bottom of the page that contains the referenced text.')
# 2 -  حاشية ختامية، سيظهر إدخالها في نهاية المستند:
builder.write('Endnote referenced main body text.')
endnote = builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote text, will appear at the very end of the document.')
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
self.assertEqual(aw.notes.FootnoteType.FOOTNOTE, footnote.footnote_type)
self.assertEqual(aw.notes.FootnoteType.ENDNOTE, endnote.footnote_type)
doc.save(file_name=ARTIFACTS_DIR + 'InlineStory.FootnoteEndnote.docx')
```

### See Also

* module [aspose.words.notes](../../)
* class [Footnote](../)

