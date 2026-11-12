---
title: PageSetup.restart_page_numbering property
linktitle: restart_page_numbering property
articleTitle: restart_page_numbering property
second_title: Aspose.Words for Python
description: "PageSetup.restart_page_numbering property. True if page numbering restarts at the beginning of the section."
type: docs
weight: 360
url: /tr/python-net/aspose.words/pagesetup/restart_page_numbering/
---

## PageSetup.restart_page_numbering property

True if page numbering restarts at the beginning of the section.


```python
@property
def restart_page_numbering(self) -> bool:
    ...

@restart_page_numbering.setter
def restart_page_numbering(self, value: bool):
    ...

```

### Remarks

If set to ``False``, the [PageSetup.restart_page_numbering](./) property will override the
[PageSetup.page_starting_number](../page_starting_number/) property so that page numbering can continue from the previous section.



### Examples

Shows how to set up page numbering in a section.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Section 1, page 1.')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Section 1, page 2.')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Section 1, page 3.')
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
builder.writeln('Section 2, page 1.')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Section 2, page 2.')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Section 2, page 3.')
# Belge oluşturucuyu ilk bölümün birincil üstbilgisine taşıyın,
# bu bölümdeki her sayfa bunu görüntüleyecek.
builder.move_to_section(0)
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_PRIMARY)
# Geçerli sayfanın numarasını gösterecek bir PAGE alanı ekleyin.
builder.write('Page ')
builder.insert_field(field_code='PAGE', field_value='')
# Bölümü, PAGE alanlarının sayımının 5'ten başlamasını sağlayacak şekilde yapılandırın.
# Ayrıca, tüm PAGE alanlarını sayfa numaralarını büyük harf Roma rakamlarıyla göstermeleri için yapılandırın.
page_setup = doc.sections[0].page_setup
page_setup.restart_page_numbering = True
page_setup.page_starting_number = 5
page_setup.page_number_style = aw.NumberStyle.UPPERCASE_ROMAN
# İkinci bölüm için başka bir birincil üstbilgi oluşturun, içinde başka bir PAGE alanı olsun.
builder.move_to_section(1)
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_PRIMARY)
builder.paragraph_format.alignment = aw.ParagraphAlignment.CENTER
builder.write(' - ')
builder.insert_field(field_code='PAGE', field_value='')
builder.write(' - ')
# Bölümü, PAGE alanlarının sayımının 10'dan başlamasını sağlayacak şekilde yapılandırın.
# Ayrıca, tüm PAGE alanlarını sayfa numaralarını Arap rakamlarıyla göstermeleri için yapılandırın.
page_setup = doc.sections[1].page_setup
page_setup.page_starting_number = 10
page_setup.restart_page_numbering = True
page_setup.page_number_style = aw.NumberStyle.ARABIC
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.PageNumbering.docx')
```

### See Also

* module [aspose.words](../../)
* class [PageSetup](../)

