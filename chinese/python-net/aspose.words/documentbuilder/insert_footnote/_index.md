---
title: DocumentBuilder.insert_footnote method
linktitle: insert_footnote method
articleTitle: insert_footnote method
second_title: Aspose.Words for Python
description: "aspose.words.DocumentBuilder.insert_footnote method"
type: docs
weight: 340
url: /zh/python-net/aspose.words/documentbuilder/insert_footnote/
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
# 插入一些文本并使用脚注标记它，默认情况下 IsAuto 属性设置为 "true"，
# 因此正文中看到的标记将自动编号为 "1"，
# 并且脚注将出现在页面底部。
builder.write('This text will be referenced by a footnote.')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote comment regarding referenced text.')
# 插入更多文本并使用自定义引用标记的尾注标记它，
# 它将替代数字 "2" 使用，并将 "IsAuto" 设置为 false。
builder.write('This text will be referenced by an endnote.')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote comment regarding referenced text.', reference_mark='CustomMark')
# 脚注始终出现在其引用文本的底部，
# 因此此分页符不会影响脚注。
# 另一方面，尾注始终位于文档的末尾
# 因此此分页符会将尾注推到下一页。
builder.insert_break(aw.BreakType.PAGE_BREAK)
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.InsertFootnote.docx')
```

## See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

