---
title: FieldSeq.bookmark_name property
linktitle: bookmark_name property
articleTitle: bookmark_name property
second_title: Aspose.Words for Python
description: "FieldSeq.bookmark_name property. Gets or sets a bookmark name that refers to an item elsewhere in the document rather than in the current location."
type: docs
weight: 20
url: /zh/python-net/aspose.words.fields/fieldseq/bookmark_name/
---

## FieldSeq.bookmark_name property

Gets or sets a bookmark name that refers to an item elsewhere in the document rather than in the current location.


```python
@property
def bookmark_name(self) -> str:
    ...

@bookmark_name.setter
def bookmark_name(self, value: str):
    ...

```

### Examples

Shows how to combine table of contents and sequence fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# TOC 域可以为文档中找到的每个 SEQ 域在目录中创建一个条目。
# 每个条目包含包含 SEQ 字段的段落，
# 以及字段出现的页码。
field_toc = builder.insert_field(field_type=FieldType.FIELD_TOC, update_field=True).as_field_toc()
# 将此 TOC 字段配置为具有值为 "MySequence" 的 SequenceIdentifier 属性。
field_toc.table_of_figures_label = 'MySequence'
# 将此 TOC 字段配置为仅获取位于书签范围内的 SEQ 字段
# 名为 "TOCBookmark" 的书签。
field_toc.bookmark_name = 'TOCBookmark'
builder.insert_break(aw.BreakType.PAGE_BREAK)
self.assertEqual(' TOC  \\c MySequence \\b TOCBookmark', field_toc.get_field_code())
# SEQ 域显示一个在每个 SEQ 域递增的计数。
# 这些域还为每个唯一命名的序列维护单独的计数
# 由 SEQ 域的 "SequenceIdentifier" 属性标识。
# 插入一个 SEQ 字段，其序列标识符匹配 TOC 的
# TableOfFiguresLabel 属性。由于该字段位于外部，它不会在 TOC 中创建条目。
# 由 "BookmarkName" 指定的书签范围。
builder.write('MySequence #')
field_seq = builder.insert_field(field_type=FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
builder.writeln(', will not show up in the TOC because it is outside of the bookmark.')
builder.start_bookmark('TOCBookmark')
# 此 SEQ 字段的序列匹配 TOC 的 "TableOfFiguresLabel" 属性，并且位于书签范围内。
# 包含此字段的段落将作为条目显示在 TOC 中。
builder.write('MySequence #')
field_seq = builder.insert_field(field_type=FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
builder.writeln(', will show up in the TOC next to the entry for the above caption.')
# 此 SEQ 字段的序列与 TOC 的 "TableOfFiguresLabel" 属性不匹配，
# 且位于书签范围内。其段落将不会作为条目显示在 TOC 中。
builder.write('MySequence #')
field_seq = builder.insert_field(field_type=FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'OtherSequence'
builder.writeln(", will not show up in the TOC because it's from a different sequence identifier.")
# 此 SEQ 字段的序列匹配 TOC 的 "TableOfFiguresLabel" 属性，并且位于书签范围内。
# 此字段还引用了另一个书签。该书签的内容将出现在此 SEQ 字段的 TOC 条目中。
# SEQ 字段本身不会显示该书签的内容。
field_seq = builder.insert_field(field_type=FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
field_seq.bookmark_name = 'SEQBookmark'
self.assertEqual(' SEQ  MySequence SEQBookmark', field_seq.get_field_code())
# 创建一个书签，其内容将因上述 SEQ 字段的引用而显示在 TOC 条目中。
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.start_bookmark('SEQBookmark')
builder.write('MySequence #')
field_seq = builder.insert_field(field_type=FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
builder.writeln(', text from inside SEQBookmark.')
builder.end_bookmark('SEQBookmark')
builder.end_bookmark('TOCBookmark')
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.SEQ.Bookmark.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldSeq](../)

