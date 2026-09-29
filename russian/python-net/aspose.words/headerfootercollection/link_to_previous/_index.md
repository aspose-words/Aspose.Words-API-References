---
title: HeaderFooterCollection.link_to_previous method
linktitle: link_to_previous method
articleTitle: link_to_previous method
second_title: Aspose.Words for Python
description: "aspose.words.HeaderFooterCollection.link_to_previous method"
type: docs
weight: 90
url: /ru/python-net/aspose.words/headerfootercollection/link_to_previous/
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
# Перейдите к первому разделу и создайте верхний и нижний колонтитулы. По умолчанию,
# верхний и нижний колонтитулы будут отображаться только на страницах раздела, в котором они находятся.
builder.move_to_section(0)
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_PRIMARY)
builder.write('This is the header, which will be displayed in sections 1 and 2.')
builder.move_to_header_footer(aw.HeaderFooterType.FOOTER_PRIMARY)
builder.write('This is the footer, which will be displayed in sections 1, 2 and 3.')
# Мы можем связать верхние/нижние колонтитулы раздела с верхними/нижними колонтитулами предыдущего раздела
# чтобы связанный раздел отображал верхние/нижние колонтитулы связанного раздела.
doc.sections[1].headers_footers.link_to_previous(is_link_to_previous=True)
# Каждый раздел всё равно будет иметь свои собственные объекты верхнего/нижнего колонтитула. Когда мы связываем разделы,
# связанный раздел будет отображать верхний/нижний колонтитул связанного раздела, сохраняя при этом свои собственные.
assert doc.sections[0].headers_footers[0] is not doc.sections[1].headers_footers[0]
assert doc.sections[0].headers_footers[0].parent_section is not doc.sections[1].headers_footers[0].parent_section
# Свяжите верхние/нижние колонтитулы третьего раздела с верхними/нижними колонтитулами второго раздела.
# Второй раздел уже связан с верхними/нижними колонтитулами первого раздела,
# поэтому связывание со вторым разделом создаст цепочку связей.
# Первый, второй и теперь третий разделы будут все отображать верхние колонтитулы первого раздела.
doc.sections[2].headers_footers.link_to_previous(is_link_to_previous=True)
# Мы можем разорвать связь верхних/нижних колонтитулов предыдущего раздела, передав "false" при вызове метода LinkToPrevious.
doc.sections[2].headers_footers.link_to_previous(is_link_to_previous=False)
# Мы также можем выбрать только определённый тип верхнего/нижнего колонтитула для связывания с помощью этого метода.
# Третий раздел теперь будет иметь такой же нижний колонтитул, как у второго и первого разделов, но не будет иметь верхний колонтитул.
doc.sections[2].headers_footers.link_to_previous(header_footer_type=aw.HeaderFooterType.FOOTER_PRIMARY, is_link_to_previous=True)
# Заголовки/нижние колонтитулы первого раздела не могут связываться ни с чем, потому что предыдущего раздела нет.
self.assertEqual(2, doc.sections[0].headers_footers.count)
self.assertEqual(2, len(list(filter(lambda hf: not hf.as_header_footer().is_linked_to_previous, doc.sections[0].headers_footers))))
# Все заголовки/нижние колонтитулы второго раздела связаны с заголовками/нижними колонтитулами первого раздела.
self.assertEqual(6, doc.sections[1].headers_footers.count)
self.assertEqual(6, len(list(filter(lambda hf: hf.as_header_footer().is_linked_to_previous, doc.sections[1].headers_footers))))
# В третьем разделе только нижний колонтитул связан с нижним колонтитулом первого раздела через второй раздел.
self.assertEqual(6, doc.sections[2].headers_footers.count)
self.assertEqual(5, len(list(filter(lambda hf: not hf.as_header_footer().is_linked_to_previous, doc.sections[2].headers_footers))))
self.assertTrue(doc.sections[2].headers_footers[3].is_linked_to_previous)
doc.save(file_name=ARTIFACTS_DIR + 'HeaderFooter.Link.docx')
```

## See Also

* module [aspose.words](../../)
* class [HeaderFooterCollection](../)

