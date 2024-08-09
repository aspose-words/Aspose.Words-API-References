---
title: Comment.date_time_utc property
linktitle: date_time_utc property
articleTitle: date_time_utc property
second_title: Aspose.Words for Python
description: "Comment.date_time_utc property. Gets the UTC date and time that the comment was made."
type: docs
weight: 50
url: /python-net/aspose.words/comment/date_time_utc/
---

## Comment.date_time_utc property

Gets the UTC date and time that the comment was made.


```python
@property
def date_time_utc(self) -> datetime.datetime:
    ...

```

### Remarks

The default value is
datetime.datetime.min



### Examples

Shows how to get UTC date and time.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
date = datetime.datetime.now()
comment = aw.Comment(doc, 'John Doe', 'J.D.', date)
comment.set_text('My comment.')
builder.current_paragraph.append_child(comment)
doc.save(file_name=ARTIFACTS_DIR + 'Comment.UtcDateTime.docx')
doc = aw.Document(ARTIFACTS_DIR + 'Comment.UtcDateTime.docx')
comment = doc.get_child(aw.NodeType.COMMENT, 0, True).as_comment()
# DateTimeUtc return data without milliseconds.
self.assertEqual(date.astimezone(timezone.utc).strftime('%Y-%m-%d %H:%M:%S'), comment.date_time_utc.strftime('%Y-%m-%d %H:%M:%S'))
```

### See Also

* module [aspose.words](../../)
* class [Comment](../)

