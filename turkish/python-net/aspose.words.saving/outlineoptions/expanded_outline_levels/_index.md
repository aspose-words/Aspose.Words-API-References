---
title: OutlineOptions.expanded_outline_levels property
linktitle: expanded_outline_levels property
articleTitle: expanded_outline_levels property
second_title: Aspose.Words for Python
description: "OutlineOptions.expanded_outline_levels property. Specifies how many levels in the document outline to show expanded when the file is viewed."
type: docs
weight: 60
url: /tr/python-net/aspose.words.saving/outlineoptions/expanded_outline_levels/
---

## OutlineOptions.expanded_outline_levels property

Specifies how many levels in the document outline to show expanded when the file is viewed.


```python
@property
def expanded_outline_levels(self) -> int:
    ...

@expanded_outline_levels.setter
def expanded_outline_levels(self, value: int):
    ...

```

### Remarks

Note that this options will not work when saving to XPS.

Specify 0 and the document outline will be collapsed; specify 1 and the first level items
in the outline will be expanded and so on.

Default is 0. Valid range is 0 to 9.




### Examples

Shows how to convert a whole document to PDF with three levels in the document outline.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 1'den 5'e kadar seviyelerde başlıklar ekleyin.
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1
self.assertTrue(builder.paragraph_format.is_heading)
builder.writeln('Heading 1')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING2
builder.writeln('Heading 1.1')
builder.writeln('Heading 1.2')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING3
builder.writeln('Heading 1.2.1')
builder.writeln('Heading 1.2.2')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING4
builder.writeln('Heading 1.2.2.1')
builder.writeln('Heading 1.2.2.2')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING5
builder.writeln('Heading 1.2.2.2.1')
builder.writeln('Heading 1.2.2.2.2')
# "PdfSaveOptions" nesnesi oluşturun; bu nesneyi belgenin "Save" metoduna geçebiliriz
# bu yöntemin belgeyi .PDF'ye nasıl dönüştürdüğünü değiştirmek için.
options = aw.saving.PdfSaveOptions()
# Çıktı PDF belgesi bir anahat içerecek; bu, belge gövdesindeki başlıkları listeleyen bir içindekiler tablosudur.
# Bu taslaktaki bir girdiye tıklamak, ilgili başlığın konumuna götürecek.
# "HeadingsOutlineLevels" özelliğini "4" olarak ayarlayarak 4'ün üzerindeki seviyedeki tüm başlıkları anahattan hariç tutun.
options.outline_options.headings_outline_levels = 4
# Bir anahat girdisinin kendisi ile aynı ya da daha düşük seviyedeki bir sonraki girdi arasında daha yüksek seviyeli sonraki girdileri varsa,
# girdinin solunda bir ok görünecektir. Bu girdi, birkaç böyle "alt-girdi"nin "sahibi"dir.
# Belgemizde, 5. başlık seviyesindeki anahat girdileri, ikinci 4. seviye anahat girdisinin alt-girdileri olarak yer alır,
# 4. ve 5. başlık seviyesi girişleri, ikinci 3. seviye girişinin alt girişleridir ve benzeri.
# Taslakta, "owner" girişinin okuna tıklayarak tüm alt girişlerini daraltabilir/genişletebiliriz.
# "ExpandedOutlineLevels" özelliğini "2" olarak ayarlayın, böylece 2. seviye ve daha altındaki tüm başlık seviyesi girişleri otomatik olarak genişler
# ve belgeyi açtığımızda seviye 3 ve üzerindeki tüm girişleri daraltın.
options.outline_options.expanded_outline_levels = 2
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.ExpandedOutlineLevels.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [OutlineOptions](../)

