---
title: FieldToc.update_page_numbers method
linktitle: update_page_numbers method
articleTitle: update_page_numbers method
second_title: Aspose.Words for Python
description: "FieldToc.update_page_numbers method. Updates the page numbers for items in this table of contents."
type: docs
weight: 180
url: /tr/python-net/aspose.words.fields/fieldtoc/update_page_numbers/
---

## update_page_numbers() {#default}

Updates the page numbers for items in this table of contents.


```python
def update_page_numbers(self):
    ...
```

### Returns

``True`` if the operation is successful. If any of the related TOC bookmarks was removed, ``False`` will be returned.



### Examples

Shows how to insert a TOC, and populate it with entries based on heading styles.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.start_bookmark('MyBookmark')
# Bir TOC alanı ekleyin, bu alan tüm başlıkları bir içindekiler tablosunda derleyecek.
# Her başlık için, bu alan sol tarafta o başlık stilindeki metinle bir satır oluşturacak,
# ve başlığın göründüğü sayfa numarasını sağ tarafta.
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_TOC, update_field=True).as_field_toc()
# Yalnızca başlıkları listelemek için BookmarkName özelliğini kullanın
# "MyBookmark" adlı bir yer işareti sınırları içinde görünen
field.bookmark_name = 'MyBookmark'
# "Heading 1" gibi yerleşik bir başlık stili uygulanmış metin bir başlık olarak sayılacak.
# Bu özellikte, TOC tarafından başlık olarak algılanacak ek stilleri ve bunların TOC seviyelerini adlandırabiliriz.
field.custom_styles = 'Quote; 6; Intense Quote; 7'
# Varsayılan olarak, Styles/TOC seviyeleri CustomStyles özelliğinde virgülle ayrılır,
# ancak bu özellikte özel bir ayırıcı belirleyebiliriz.
doc.field_options.custom_toc_style_separator = ';'
# Bu aralığın dışındaki TOC seviyelerine sahip başlıkları dışlamak için alanı yapılandırın.
field.heading_level_range = '1-3'
# TOC, TOC seviyeleri bu aralık içinde olan başlıkların sayfa numaralarını göstermez.
field.page_number_omitting_level_range = '2-5'
# Her başlığı sayfa numarasından ayıracak özel bir dize ayarlayın.
field.entry_separator = '-'
field.insert_hyperlinks = True
field.hide_in_web_layout = False
field.preserve_line_breaks = True
field.preserve_tabs = True
field.use_paragraph_outline_level = False
self.insert_new_page_with_heading(builder, 'First entry', 'Heading 1')
builder.writeln('Paragraph text.')
self.insert_new_page_with_heading(builder, 'Second entry', 'Heading 1')
self.insert_new_page_with_heading(builder, 'Third entry', 'Quote')
self.insert_new_page_with_heading(builder, 'Fourth entry', 'Intense Quote')
# Bu iki başlığın sayfa numaraları atlanacak çünkü "2-5" aralığı içinde bulunuyorlar.
self.insert_new_page_with_heading(builder, 'Fifth entry', 'Heading 2')
self.insert_new_page_with_heading(builder, 'Sixth entry', 'Heading 3')
# Bu giriş görünmez çünkü "Heading 4" daha önce ayarladığımız "1-3" aralığının dışındadır.
self.insert_new_page_with_heading(builder, 'Seventh entry', 'Heading 4')
builder.end_bookmark('MyBookmark')
builder.writeln('Paragraph text.')
# This entry does not appear because it is outside the bookmark specified by the TOC.
self.insert_new_page_with_heading(builder, 'Eighth entry', 'Heading 1')
self.assertEqual(' TOC  \\b MyBookmark \\t "Quote; 6; Intense Quote; 7" \\o 1-3 \\n 2-5 \\p - \\h \\u0000 \\w', field.get_field_code())
field.update_page_numbers()
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.TOC.docx')
```

Shows how to insert a TOC, and populate it with entries based on heading styles (InsertNewPageWithHeading).

```python
def insert_new_page_with_heading(self, builder, caption_text, style_name):
    builder.insert_break(aw.BreakType.PAGE_BREAK)
    original_style = builder.paragraph_format.style_name
    builder.paragraph_format.style = builder.document.styles.get_by_name(style_name)
    builder.writeln(caption_text)
    builder.paragraph_format.style = builder.document.styles.get_by_name(original_style)
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldToc](../)

