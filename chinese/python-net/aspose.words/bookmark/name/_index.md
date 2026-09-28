---
title: Bookmark.name property
linktitle: name property
articleTitle: name property
second_title: Aspose.Words for Python
description: "Bookmark.name property. Gets or sets the name of the bookmark."
type: docs
weight: 60
url: /zh/python-net/aspose.words/bookmark/name/
---

## Bookmark.name property

Gets or sets the name of the bookmark.


```python
@property
def name(self) -> str:
    ...

@name.setter
def name(self, value: str):
    ...

```

### Remarks

Note that if you change the name of a bookmark to a name that already exists in the document,
no error will be given and only the first bookmark will be stored when you save the document.


### Examples

Shows how to insert a bookmark.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 有效的书签具有名称、BookmarkStart 和 BookmarkEnd 节点。
# 如果使用 Microsoft Word 打开已保存的文档，书签名称中的任何空白字符都会被转换为下划线。
# 如果我们在 Microsoft Word 中通过 插入 -> 链接 -> 书签 高亮书签名称，并按 "Go To"，
# 光标将跳转到 BookmarkStart 和 BookmarkEnd 节点之间包围的文本。
builder.start_bookmark('My Bookmark')
builder.write('Contents of MyBookmark.')
builder.end_bookmark('My Bookmark')
# 书签存储在此集合中。
self.assertEqual('My Bookmark', doc.range.bookmarks[0].name)
doc.save(file_name=ARTIFACTS_DIR + 'Bookmarks.Insert.docx')
```

### See Also

* module [aspose.words](../../)
* class [Bookmark](../)

