---
title: Comment constructor
second_title: Aspose.Words for Python via .NET API Reference
description: "aspose.words.Comment constructor"
type: docs
weight: 10
url: /python-net/aspose.words/comment/__init__/
---

## Comment(doc) {#documentbase}

Initializes a new instance of the **Comment** class.



```python
def __init__(self, doc: aspose.words.DocumentBase):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| doc | [DocumentBase](../../documentbase/) |  |

When **Comment** is created, it belongs to the specified document, but is not
yet part of the document and **ParentNode** is null.

To append **Comment** to the document use InsertAfter or InsertBefore
on the paragraph where you want the comment inserted.

After creating a comment, don't forget to set its [Comment.author](../author/),
[Comment.initial](../initial/) and [Comment.date_time](../date_time/) properties.




## Comment(doc, author, initial, date_time) {#documentbase_str_str_datetime}

Initializes a new instance of the **Comment** class.



```python
def __init__(self, doc: aspose.words.DocumentBase, author: str, initial: str, date_time: datetime):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| doc | [DocumentBase](../../documentbase/) |  |
| author | str |  |
| initial | str |  |
| date_time | datetime |  |

## Examples

Shows how to add a comment to a paragraph.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.write("Hello world!")

comment = aw.Comment(doc, "John Doe", "JD", date.today())
builder.current_paragraph.append_child(comment)
builder.move_to(comment.append_child(aw.Paragraph(doc)))
builder.write("Comment text.")

self.assertEqual(date.today(), comment.date_time.date())

# In Microsoft Word, we can right-click this comment in the document body to edit it, or reply to it.
doc.save(ARTIFACTS_DIR + "InlineStory.add_comment.docx")
```

## See Also

* module [aspose.words](../../)
* class [Comment](../)

