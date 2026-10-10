---
title: Document.first_section property
linktitle: first_section property
articleTitle: first_section property
second_title: Aspose.Words for Python
description: "Document.first_section property. Gets the first section in the document."
type: docs
weight: 140
url: /zh/python-net/aspose.words/document/first_section/
---

## Document.first_section property

Gets the first section in the document.


```python
@property
def first_section(self) -> aspose.words.Section:
    ...

```

### Remarks

Returns ``None`` if there are no sections.



### Examples

Shows how to replace text in a document's footer.

```python
doc = aw.Document(file_name=MY_DIR + 'Footer.docx')
headers_footers = doc.first_section.headers_footers
footer = headers_footers.get_by_header_footer_type(aw.HeaderFooterType.FOOTER_PRIMARY)
options = aw.replacing.FindReplaceOptions()
options.match_case = False
options.find_whole_words_only = False
current_year = datetime.datetime.now().year
footer.range.replace(pattern='(C) 2006 Aspose Pty Ltd.', replacement=f'Copyright (C) {current_year} by Aspose Pty Ltd.', options=options)
doc.save(file_name=ARTIFACTS_DIR + 'HeaderFooter.ReplaceText.docx')
```

Shows how to create a new section with a document builder.

```python
doc = aw.Document()
# 空白文档默认包含一个节，
# 该节包含我们可以编辑的子节点。
self.assertEqual(1, doc.sections.count)
# 使用文档生成器向第一个节添加文本。
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Hello world!')
# 通过插入节分隔符创建第二个节。
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
self.assertEqual(2, doc.sections.count)
# 每个节都有自己的页面设置。
# 我们可以将第二个节中的文本分成两列。
# 这不会影响第一个节中的文本。
doc.last_section.page_setup.text_columns.set_count(2)
builder.writeln('Column 1.')
builder.insert_break(aw.BreakType.COLUMN_BREAK)
builder.writeln('Column 2.')
self.assertEqual(1, doc.first_section.page_setup.text_columns.count)
self.assertEqual(2, doc.last_section.page_setup.text_columns.count)
doc.save(file_name=ARTIFACTS_DIR + 'Section.Create.docx')
```

Shows how to iterate through the children of a composite node.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.write('Section 1')
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_PRIMARY)
builder.write('Primary header')
builder.move_to_header_footer(aw.HeaderFooterType.FOOTER_PRIMARY)
builder.write('Primary footer')
section = doc.first_section
# Section 是一个复合节点，可以包含子节点，
# 但仅当这些子节点是 "Body" 或 "HeaderFooter" 类型时。
for node in section:
    switch_condition = node.node_type
    if switch_condition == aw.NodeType.BODY:
        body = node.as_body()
        print('Body:')
        print(f'\t"{body.get_text().strip()}"')
    elif switch_condition == aw.NodeType.HEADER_FOOTER:
        header_footer = node.as_header_footer()
        print(f'HeaderFooter type: {header_footer.header_footer_type}:')
        print(f'\t"{header_footer.get_text().strip()}"')
    else:
        raise Exception('Unexpected node type in a section.')
```

### See Also

* module [aspose.words](../../)
* class [Document](../)

