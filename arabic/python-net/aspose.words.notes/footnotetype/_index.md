---
title: FootnoteType enumeration
linktitle: FootnoteType enumeration
articleTitle: FootnoteType enumeration
second_title: Aspose.Words for Python
description: "aspose.words.notes.FootnoteType enumeration. Specifies whether this is a footnote or an endnote."
type: docs
weight: 100
url: /ar/python-net/aspose.words.notes/footnotetype/
---

## FootnoteType enumeration

Specifies whether this is a footnote or an endnote.

Both footnotes and endnotes are represented by objects by the [FootnoteType.FOOTNOTE](./#FOOTNOTE)
class. Use [Footnote.footnote_type](../footnote/footnote_type/) to distinguish between footnotes 
and endnotes.




### Members

| Name | Description |
| --- | --- |
| FOOTNOTE | The object is a footnote. |
| ENDNOTE | The object is an endnote. |

### Examples

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

Shows how to insert and customize footnotes.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# أضف نصًا، وأشر إليه بحاشية. ستضع هذه الحاشية علامة مرجعية صغيرة مرتفعة
# بعد النص الذي تشير إليه وتُنشئ مدخلاً أسفل النص الرئيسي في أسفل الصفحة.
# سيحتوي هذا المدخل على علامة مرجعية الحاشية والنص المرجعي،
# والتي سنمررها إلى طريقة "InsertFootnote" في منشئ المستند.
builder.write('Main body text.')
footnote = builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote text.')
# إذا تم ضبط هذه الخاصية على "true"، فإن علامة مرجعية حاشيتنا
# ستكون مؤشرها بين جميع حواشي القسم.
# هذه هي الحاشية الأولى، لذا ستكون علامة المرجع "1".
self.assertTrue(footnote.is_auto)
# يمكننا نقل منشئ المستند داخل الحاشية لتعديل نص المرجع الخاص بها.
builder.move_to(footnote.first_paragraph)
builder.write(' More text added by a DocumentBuilder.')
builder.move_to_document_end()
self.assertEqual('\x02 Footnote text. More text added by a DocumentBuilder.', footnote.get_text().strip())
builder.write(' More main body text.')
footnote = builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote text.')
# يمكننا ضبط علامة مرجعية مخصصة ستستخدمها الحاشية بدلاً من رقم مؤشرها.
footnote.reference_mark = 'RefMark'
self.assertFalse(footnote.is_auto)
# الإشارة المرجعية التي تحتوي على العلم "IsAuto" مضبوط على true ستظل تُظهر الفهرس الحقيقي لها
# حتى إذا كانت الإشارات المرجعية السابقة تعرض علامات مرجعية مخصصة، لذا فإن علامة المرجع لهذه الإشارة ستكون "3".
builder.write(' More main body text.')
footnote = builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote text.')
self.assertTrue(footnote.is_auto)
doc.save(file_name=ARTIFACTS_DIR + 'InlineStory.AddFootnote.docx')
```

### See Also

* module [aspose.words.notes](../)
* enum value [FootnoteType.FOOTNOTE](./#FOOTNOTE)

