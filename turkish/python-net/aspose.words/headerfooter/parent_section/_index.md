---
title: HeaderFooter.parent_section property
linktitle: parent_section property
articleTitle: parent_section property
second_title: Aspose.Words for Python
description: "HeaderFooter.parent_section property. Gets the parent section of this story."
type: docs
weight: 60
url: /tr/python-net/aspose.words/headerfooter/parent_section/
---

## HeaderFooter.parent_section property

Gets the parent section of this story.


```python
@property
def parent_section(self) -> aspose.words.Section:
    ...

```

### Remarks

[HeaderFooter.parent_section](./) is equivalent to [Node.parent_node](../../node/parent_node/) casted to [Section](../../section/).




### Examples

Shows how to link headers and footers between sections.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.write('Section 1')
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
builder.write('Section 2')
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
builder.write('Section 3')
# İlk bölüme gidin ve bir üstbilgi ile bir altbilgi oluşturun. Varsayılan olarak,
# üstbilgi ve altbilgi yalnızca onları içeren bölümdeki sayfalarda görünecek.
builder.move_to_section(0)
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_PRIMARY)
builder.write('This is the header, which will be displayed in sections 1 and 2.')
builder.move_to_header_footer(aw.HeaderFooterType.FOOTER_PRIMARY)
builder.write('This is the footer, which will be displayed in sections 1, 2 and 3.')
# Bir bölümün üstbilgi/altbilgilerini önceki bölümün üstbilgi/altbilgilerine bağlayabiliriz
# bağlama bölümünün, bağlanan bölümün üstbilgi/altbilgilerini görüntülemesine izin vermek için.
doc.sections[1].headers_footers.link_to_previous(is_link_to_previous=True)
# Her bölüm hâlâ kendi üstbilgi/altbilgi nesnelerine sahip olacak. Bölümleri bağladığımızda,
# bağlama bölümü, kendi üstbilgi/altbilgilerini korurken bağlanan bölümün üstbilgi/altbilgilerini gösterecek.
assert doc.sections[0].headers_footers[0] is not doc.sections[1].headers_footers[0]
assert doc.sections[0].headers_footers[0].parent_section is not doc.sections[1].headers_footers[0].parent_section
# Üçüncü bölümün üstbilgi/altbilgilerini ikinci bölümün üstbilgi/altbilgilerine bağlayın.
# İkinci bölüm zaten birinci bölümün üstbilgi/altbilgilerine bağlı,
# bu yüzden ikinci bölüme bağlamak bir bağ zinciri oluşturacak.
# Birinci, ikinci ve artık üçüncü bölümler, birinci bölümün üstbilgilerini gösterecek.
doc.sections[2].headers_footers.link_to_previous(is_link_to_previous=True)
# LinkToPrevious metodunu çağırırken "false" geçirerek önceki bir bölümün üstbilgi/altbilgilerini bağlantısını kaldırabiliriz.
doc.sections[2].headers_footers.link_to_previous(is_link_to_previous=False)
# Bu yöntemi kullanarak yalnızca belirli bir tür üstbilgi/altbilgi seçip bağlayabiliriz.
# Üçüncü bölüm artık ikinci ve birinci bölümlerle aynı altbilgiye sahip olacak, ancak üstbilgiye sahip olmayacak.
doc.sections[2].headers_footers.link_to_previous(header_footer_type=aw.HeaderFooterType.FOOTER_PRIMARY, is_link_to_previous=True)
# İlk bölümün üstbilgi/altbilgileri, önceki bir bölüm olmadığı için kendilerini hiçbir şeye bağlayamaz.
self.assertEqual(2, doc.sections[0].headers_footers.count)
self.assertEqual(2, len(list(filter(lambda hf: not hf.as_header_footer().is_linked_to_previous, doc.sections[0].headers_footers))))
# İkinci bölümün tüm üstbilgi/altbilgileri, ilk bölümün üstbilgi/altbilgelerine bağlanmıştır.
self.assertEqual(6, doc.sections[1].headers_footers.count)
self.assertEqual(6, len(list(filter(lambda hf: hf.as_header_footer().is_linked_to_previous, doc.sections[1].headers_footers))))
# Üçüncü bölümde, yalnızca altbilgi, ikinci bölüm aracılığıyla ilk bölümün altbilgisine bağlanır.
self.assertEqual(6, doc.sections[2].headers_footers.count)
self.assertEqual(5, len(list(filter(lambda hf: not hf.as_header_footer().is_linked_to_previous, doc.sections[2].headers_footers))))
self.assertTrue(doc.sections[2].headers_footers[3].is_linked_to_previous)
doc.save(file_name=ARTIFACTS_DIR + 'HeaderFooter.Link.docx')
```

### See Also

* module [aspose.words](../../)
* class [HeaderFooter](../)

