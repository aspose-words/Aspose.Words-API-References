---
title: InlineStory.parent_paragraph property
linktitle: parent_paragraph property
articleTitle: parent_paragraph property
second_title: Aspose.Words for Python
description: "InlineStory.parent_paragraph property. Retrieves the parent [Paragraph](../../paragraph/) of this node."
type: docs
weight: 90
url: /tr/python-net/aspose.words/inlinestory/parent_paragraph/
---

## InlineStory.parent_paragraph property

Retrieves the parent [Paragraph](../../paragraph/) of this node.



```python
@property
def parent_paragraph(self) -> aspose.words.Paragraph:
    ...

```

### Examples

Shows how to insert InlineStory nodes.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
footnote = builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text=None)
# Tablo düğümlerinin, tablonun en az bir hücreye sahip olmasını sağlayan bir "EnsureMinimum()" yöntemi vardır.
table = aw.tables.Table(doc)
table.ensure_minimum()
# Bir tabloyu dipnot içinde yerleştirebiliriz, bu da tablonun referans sayfasının altbilgisinde görünmesini sağlar.
self.assertEqual(0, footnote.tables.count)
footnote.append_child(table)
self.assertEqual(1, footnote.tables.count)
self.assertEqual(aw.NodeType.TABLE, footnote.last_child.node_type)
# Bir InlineStory'nin de bir "EnsureMinimum()" yöntemi vardır, ancak bu durumda,
# düğümün son çocuğunun bir paragraf olmasını sağlar,
# Microsoft Word'de kolayca tıklayıp metin yazabilmemiz için.
footnote.ensure_minimum()
self.assertEqual(aw.NodeType.PARAGRAPH, footnote.last_child.node_type)
# Küçük üst simge numarası olan ankrajın görünümünü düzenleyin
# dipnota işaret eden ana metinde.
footnote.font.name = 'Arial'
footnote.font.color = aspose.pydrawing.Color.green
# Tüm inline story düğümlerinin kendi hikaye türleri vardır.
self.assertEqual(aw.StoryType.FOOTNOTES, footnote.story_type)
# Bir yorum, başka bir inline story türüdür.
comment = builder.current_paragraph.append_child(aw.Comment(doc=doc, author='John Doe', initial='J. D.', date_time=datetime.datetime.now())).as_comment()
# Bir inline story düğümünün üst paragrafı, ana belge gövdesinden gelen paragraf olacaktır.
self.assertEqual(doc.first_section.body.first_paragraph, comment.parent_paragraph)
# Ancak, son paragraf yorum metni içeriğinden gelen paragraftır,
# bu da ana belge gövdesinin dışındaki bir konuşma balonunda olacaktır.
# Bir yorum varsayılan olarak hiçbir alt düğüme sahip olmayacaktır,
# bu yüzden burada da bir paragraf yerleştirmek için EnsureMinimum() yöntemini uygulayabiliriz.
self.assertIsNone(comment.last_paragraph)
comment.ensure_minimum()
self.assertEqual(aw.NodeType.PARAGRAPH, comment.last_child.node_type)
# Bir paragraf elde ettiğimizde, oluşturucuyu hareket ettirerek bunu yapabilir ve yorumumuzu yazabiliriz.
builder.move_to(comment.last_paragraph)
builder.write('My comment.')
self.assertEqual(aw.StoryType.COMMENTS, comment.story_type)
doc.save(file_name=ARTIFACTS_DIR + 'InlineStory.InsertInlineStoryNodes.docx')
```

### See Also

* module [aspose.words](../../)
* class [InlineStory](../)

