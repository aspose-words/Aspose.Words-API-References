---
title: HeaderFooterCollection.link_to_previous method
linktitle: link_to_previous method
articleTitle: link_to_previous method
second_title: Aspose.Words for Python
description: "aspose.words.HeaderFooterCollection.link_to_previous method"
type: docs
weight: 90
url: /ar/python-net/aspose.words/headerfootercollection/link_to_previous/
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
# انتقل إلى القسم الأول وأنشئ رأسًا وتذييلًا. بشكل افتراضي،
# سوف يظهر الرأس والتذييل فقط على الصفحات في القسم الذي يحتويهما.
builder.move_to_section(0)
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_PRIMARY)
builder.write('This is the header, which will be displayed in sections 1 and 2.')
builder.move_to_header_footer(aw.HeaderFooterType.FOOTER_PRIMARY)
builder.write('This is the footer, which will be displayed in sections 1, 2 and 3.')
# يمكننا ربط رؤوس/تذييلات القسم بالرؤوس/التذييلات الخاصة بالقسم السابق
# للسماح للقسم المرتبط بعرض رؤوس/تذييلات القسم المرتبط.
doc.sections[1].headers_footers.link_to_previous(is_link_to_previous=True)
# كل قسم سيظل يمتلك كائنات الرأس/التذييل الخاصة به. عندما نقوم بربط الأقسام،
# القسم المرتبط سيعرض رأس/تذييلات القسم المرتبط مع الحفاظ على خاصته.
assert doc.sections[0].headers_footers[0] is not doc.sections[1].headers_footers[0]
assert doc.sections[0].headers_footers[0].parent_section is not doc.sections[1].headers_footers[0].parent_section
# ربط رؤوس/تذييلات القسم الثالث إلى رؤوس/تذييلات القسم الثاني.
# القسم الثاني بالفعل يربط إلى رؤوس/تذييلات القسم الأول،
# لذلك ربط إلى القسم الثاني سيخلق سلسلة ربط.
# القسم الأول، الثاني، والآن الثالث سيعرضون جميعًا رؤوس القسم الأول.
doc.sections[2].headers_footers.link_to_previous(is_link_to_previous=True)
# يمكننا إلغاء ربط رؤوس/تذييلات قسم سابق بتمرير "false" عند استدعاء الطريقة LinkToPrevious.
doc.sections[2].headers_footers.link_to_previous(is_link_to_previous=False)
# يمكننا أيضًا اختيار نوع محدد فقط من الرأس/التذييل للربط باستخدام هذه الطريقة.
# القسم الثالث الآن سيحصل على نفس التذييل كما في القسمين الثاني والأول، لكن ليس الرأس.
doc.sections[2].headers_footers.link_to_previous(header_footer_type=aw.HeaderFooterType.FOOTER_PRIMARY, is_link_to_previous=True)
# لا يمكن للرؤوس/التذييلات في القسم الأول ربط نفسها بأي شيء لأنه لا يوجد قسم سابق.
self.assertEqual(2, doc.sections[0].headers_footers.count)
self.assertEqual(2, len(list(filter(lambda hf: not hf.as_header_footer().is_linked_to_previous, doc.sections[0].headers_footers))))
# جميع رؤوس/تذييلات القسم الثاني مرتبطة برؤوس/تذييلات القسم الأول.
self.assertEqual(6, doc.sections[1].headers_footers.count)
self.assertEqual(6, len(list(filter(lambda hf: hf.as_header_footer().is_linked_to_previous, doc.sections[1].headers_footers))))
# في القسم الثالث، فقط التذييل مرتبط بتذييل القسم الأول عبر القسم الثاني.
self.assertEqual(6, doc.sections[2].headers_footers.count)
self.assertEqual(5, len(list(filter(lambda hf: not hf.as_header_footer().is_linked_to_previous, doc.sections[2].headers_footers))))
self.assertTrue(doc.sections[2].headers_footers[3].is_linked_to_previous)
doc.save(file_name=ARTIFACTS_DIR + 'HeaderFooter.Link.docx')
```

## See Also

* module [aspose.words](../../)
* class [HeaderFooterCollection](../)

