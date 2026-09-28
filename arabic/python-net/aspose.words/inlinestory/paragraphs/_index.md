---
title: InlineStory.paragraphs property
linktitle: paragraphs property
articleTitle: paragraphs property
second_title: Aspose.Words for Python
description: "InlineStory.paragraphs property. Gets a collection of paragraphs that are immediate children of the story."
type: docs
weight: 80
url: /ar/python-net/aspose.words/inlinestory/paragraphs/
---

## InlineStory.paragraphs property

Gets a collection of paragraphs that are immediate children of the story.


```python
@property
def paragraphs(self) -> aspose.words.ParagraphCollection:
    ...

```

### Examples

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

Shows how to add a comment to a paragraph.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.write('Hello world!')
comment = aw.Comment(doc, 'John Doe', 'JD', date.today())
builder.current_paragraph.append_child(comment)
builder.move_to(comment.append_child(aw.Paragraph(doc)))
builder.write('Comment text.')
self.assertEqual(date.today(), comment.date_time.date())
# في Microsoft Word، يمكننا النقر بزر الفأرة الأيمن على هذا التعليق في جسم المستند لتعديله أو الرد عليه.
doc.save(ARTIFACTS_DIR + 'InlineStory.add_comment.docx')
```

### See Also

* module [aspose.words](../../)
* class [InlineStory](../)

