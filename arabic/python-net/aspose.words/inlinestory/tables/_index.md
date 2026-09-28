---
title: InlineStory.tables property
linktitle: tables property
articleTitle: tables property
second_title: Aspose.Words for Python
description: "InlineStory.tables property. Gets a collection of tables that are immediate children of the story."
type: docs
weight: 110
url: /ar/python-net/aspose.words/inlinestory/tables/
---

## InlineStory.tables property

Gets a collection of tables that are immediate children of the story.


```python
@property
def tables(self) -> aspose.words.tables.TableCollection:
    ...

```

### Examples

Shows how to insert InlineStory nodes.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
footnote = builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text=None)
# عقد الجداول تحتوي على طريقة "EnsureMinimum()" التي تضمن أن الجدول يحتوي على خلية واحدة على الأقل.
table = aw.tables.Table(doc)
table.ensure_minimum()
# يمكننا وضع جدول داخل حاشية، مما سيجعله يظهر في تذييل الصفحة المرجعية.
self.assertEqual(0, footnote.tables.count)
footnote.append_child(table)
self.assertEqual(1, footnote.tables.count)
self.assertEqual(aw.NodeType.TABLE, footnote.last_child.node_type)
# قصة InlineStory لديها طريقة "EnsureMinimum()" أيضًا، ولكن في هذه الحالة،
# تضمن أن الطفل الأخير للعقدة هو فقرة،
# لكي نتمكن من النقر وكتابة النص بسهولة في Microsoft Word.
footnote.ensure_minimum()
self.assertEqual(aw.NodeType.PARAGRAPH, footnote.last_child.node_type)
# حرّر مظهر المرساة، وهي الرقم الصغير المرتفع
# في النص الرئيسي الذي يشير إلى الحاشية.
footnote.font.name = 'Arial'
footnote.font.color = aspose.pydrawing.Color.green
# جميع عقد القصة المتضمنة لديها أنواع القصة الخاصة بها.
self.assertEqual(aw.StoryType.FOOTNOTES, footnote.story_type)
# التعليق هو نوع آخر من القصة المتضمنة.
comment = builder.current_paragraph.append_child(aw.Comment(doc=doc, author='John Doe', initial='J. D.', date_time=datetime.datetime.now())).as_comment()
# الفقرة الأصلية لعقدة قصة متضمنة ستكون تلك الموجودة في جسم المستند الرئيسي.
self.assertEqual(doc.first_section.body.first_paragraph, comment.parent_paragraph)
# مع ذلك، الفقرة الأخيرة هي تلك الموجودة في محتوى نص التعليق،
# والتي ستكون خارج جسم المستند الرئيسي داخل فقاعة حوار.
# التعليق لن يحتوي على أي عقد فرعية بشكل افتراضي،
# لذا يمكننا تطبيق طريقة EnsureMinimum() لوضع فقرة هنا أيضًا.
self.assertIsNone(comment.last_paragraph)
comment.ensure_minimum()
self.assertEqual(aw.NodeType.PARAGRAPH, comment.last_child.node_type)
# بمجرد أن نحصل على فقرة، يمكننا نقل الباني للقيام بذلك وكتابة تعليقنا.
builder.move_to(comment.last_paragraph)
builder.write('My comment.')
self.assertEqual(aw.StoryType.COMMENTS, comment.story_type)
doc.save(file_name=ARTIFACTS_DIR + 'InlineStory.InsertInlineStoryNodes.docx')
```

### See Also

* module [aspose.words](../../)
* class [InlineStory](../)

