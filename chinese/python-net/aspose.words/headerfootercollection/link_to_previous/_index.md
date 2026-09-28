---
title: HeaderFooterCollection.link_to_previous method
linktitle: link_to_previous method
articleTitle: link_to_previous method
second_title: Aspose.Words for Python
description: "aspose.words.HeaderFooterCollection.link_to_previous method"
type: docs
weight: 90
url: /zh/python-net/aspose.words/headerfootercollection/link_to_previous/
---

## link_to_previous(is_link_to_previous) {#bool}

Links or unlinks all headers and footers to the corresponding
headers and footers in the previous section.


```python
def link_to_previous(self, is_link_to_previous: bool):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| is_link_to_previous | bool | ``True`` to link the headers and footers to the previous section; ``False`` to unlink them. |

### Remarks

If any of the headers or footers do not exist, creates them automatically.




## link_to_previous(header_footer_type, is_link_to_previous) {#headerfootertype_bool}

Links or unlinks the specified header or footer to the corresponding
header or footer in the previous section.


```python
def link_to_previous(self, header_footer_type: aspose.words.HeaderFooterType, is_link_to_previous: bool):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| header_footer_type | [HeaderFooterType](../../headerfootertype/) | A [HeaderFooterType](../../headerfootertype/) value that specifies the header or footer to link/unlink. |
| is_link_to_previous | bool | ``True`` to link the header or footer to the previous section; ``False`` to unlink. |

### Remarks

If the header or footer of the specified type does not exist, creates it automatically.




## Examples

Shows how to link headers and footers between sections.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.write('Section 1')
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
builder.write('Section 2')
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
builder.write('Section 3')
# 移动到第一节并创建页眉和页脚。默认情况下，
# 页眉和页脚仅会出现在包含它们的章节页面上。
builder.move_to_section(0)
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_PRIMARY)
builder.write('This is the header, which will be displayed in sections 1 and 2.')
builder.move_to_header_footer(aw.HeaderFooterType.FOOTER_PRIMARY)
builder.write('This is the footer, which will be displayed in sections 1, 2 and 3.')
# 我们可以将章节的页眉/页脚链接到前一章节的页眉/页脚
# 以便链接的章节显示被链接章节的页眉/页脚。
doc.sections[1].headers_footers.link_to_previous(is_link_to_previous=True)
# 每个章节仍然拥有自己的页眉/页脚对象。当我们链接章节时，
# 链接的章节将在保留自己的同时显示被链接章节的页眉/页脚。
assert doc.sections[0].headers_footers[0] is not doc.sections[1].headers_footers[0]
assert doc.sections[0].headers_footers[0].parent_section is not doc.sections[1].headers_footers[0].parent_section
# 将第三节的页眉/页脚链接到第二节的页眉/页脚。
# 第二节已经链接到第一节的页眉/页脚，
# 因此链接到第二节将形成一个链接链。
# 第一、第二以及现在的第三节都将显示第一节的页眉。
doc.sections[2].headers_footers.link_to_previous(is_link_to_previous=True)
# 我们可以在调用 LinkToPrevious 方法时传入 "false" 来取消链接前一节的页眉/页脚。
doc.sections[2].headers_footers.link_to_previous(is_link_to_previous=False)
# 我们还可以使用此方法仅选择特定类型的页眉/页脚进行链接。
# 现在第三节将拥有与第二节和第一节相同的页脚，但不包含页眉。
doc.sections[2].headers_footers.link_to_previous(header_footer_type=aw.HeaderFooterType.FOOTER_PRIMARY, is_link_to_previous=True)
# 由于没有前一节，第一节的页眉/页脚无法链接到任何内容。
self.assertEqual(2, doc.sections[0].headers_footers.count)
self.assertEqual(2, len(list(filter(lambda hf: not hf.as_header_footer().is_linked_to_previous, doc.sections[0].headers_footers))))
# 第二节的所有页眉/页脚都链接到第一节的页眉/页脚。
self.assertEqual(6, doc.sections[1].headers_footers.count)
self.assertEqual(6, len(list(filter(lambda hf: hf.as_header_footer().is_linked_to_previous, doc.sections[1].headers_footers))))
# 在第三节中，只有页脚通过第二节链接到第一节的页脚。
self.assertEqual(6, doc.sections[2].headers_footers.count)
self.assertEqual(5, len(list(filter(lambda hf: not hf.as_header_footer().is_linked_to_previous, doc.sections[2].headers_footers))))
self.assertTrue(doc.sections[2].headers_footers[3].is_linked_to_previous)
doc.save(file_name=ARTIFACTS_DIR + 'HeaderFooter.Link.docx')
```

## See Also

* module [aspose.words](../../)
* class [HeaderFooterCollection](../)

