---
title: FindReplaceOptions.ignore_inserted property
linktitle: ignore_inserted property
articleTitle: ignore_inserted property
second_title: Aspose.Words for Python
description: "FindReplaceOptions.ignore_inserted property. Gets or sets a boolean value indicating either to ignore text inside insert revisions"
type: docs
weight: 100
url: /zh/python-net/aspose.words.replacing/findreplaceoptions/ignore_inserted/
---

## FindReplaceOptions.ignore_inserted property

Gets or sets a boolean value indicating either to ignore text inside insert revisions.
The default value is ``False``.



```python
@property
def ignore_inserted(self) -> bool:
    ...

@ignore_inserted.setter
def ignore_inserted(self, value: bool):
    ...

```

### Examples

Shows how to include or ignore text inside insert revisions during a find-and-replace operation.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Hello world!')
# 开始跟踪修订并插入一个段落。该段落将成为插入修订。
doc.start_track_revisions(author='John Doe', date_time=datetime.datetime.now())
builder.writeln('Hello again!')
doc.stop_track_revisions()
self.assertTrue(doc.first_section.body.paragraphs[1].is_insert_revision)
# 我们可以使用 "FindReplaceOptions" 对象来修改查找替换过程。
options = aw.replacing.FindReplaceOptions()
# 将 "IgnoreInserted" 标志设置为 "true" 以进行查找替换
# 操作时忽略作为插入修订的段落。
# 将 "IgnoreInserted" 标志设置为 "false" 以进行查找替换
# 操作时也搜索插入修订中的文本。
options.ignore_inserted = ignore_text_inside_insert_revisions
doc.range.replace(pattern='Hello', replacement='Greetings', options=options)
self.assertEqual('Greetings world!\rHello again!' if ignore_text_inside_insert_revisions else 'Greetings world!\rGreetings again!', doc.get_text().strip())
```

### See Also

* module [aspose.words.replacing](../../)
* class [FindReplaceOptions](../)

