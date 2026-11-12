---
title: OutlineOptions.create_missing_outline_levels property
linktitle: create_missing_outline_levels property
articleTitle: create_missing_outline_levels property
second_title: Aspose.Words for Python
description: "OutlineOptions.create_missing_outline_levels property. Gets or sets a value determining whether or not to create missing outline levels when the document is  exported."
type: docs
weight: 30
url: /tr/python-net/aspose.words.saving/outlineoptions/create_missing_outline_levels/
---

## OutlineOptions.create_missing_outline_levels property

Gets or sets a value determining whether or not to create missing outline levels when the document is 
exported.

Default value for this property is ``False``.




```python
@property
def create_missing_outline_levels(self) -> bool:
    ...

@create_missing_outline_levels.setter
def create_missing_outline_levels(self, value: bool):
    ...

```

### Examples

Shows how to work with outline levels that do not contain any corresponding headings when saving a PDF document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Seviye 1 ve 5 için TOC girdileri olarak hizmet edebilecek başlıklar ekleyin.
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1
self.assertTrue(builder.paragraph_format.is_heading)
builder.writeln('Heading 1')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING5
builder.writeln('Heading 1.1.1.1.1')
builder.writeln('Heading 1.1.1.1.2')
# "PdfSaveOptions" nesnesi oluşturun; bu nesneyi belgenin "Save" metoduna geçebiliriz
# bu yöntemin belgeyi .PDF'ye nasıl dönüştürdüğünü değiştirmek için.
save_options = aw.saving.PdfSaveOptions()
# Çıktı PDF belgesi bir anahat içerecek; bu, belge gövdesindeki başlıkları listeleyen bir içindekiler tablosudur.
# Bu taslaktaki bir girdiye tıklamak, ilgili başlığın konumuna götürecek.
# Özet içinde seviye 5 ve altındaki tüm başlıkları dahil etmek için "HeadingsOutlineLevels" özelliğini "5" olarak ayarlayın.
save_options.outline_options.headings_outline_levels = 5
# Bu belge, seviye 1 ve 5 başlıkları içerir ve seviye 2, 3 ve 4 başlıkları içermez.
# Çıktı PDF belgesi, özet seviyelerini 2, 3 ve 4'ü "eksik" olarak değerlendirecek.
# "CreateMissingOutlineLevels" özelliğini "true" olarak ayarlayarak eksik tüm seviyeleri özet içine dahil edin,
# kullanılabilir başlık olmadığı için boş özet girdileri bırakır.
# "CreateMissingOutlineLevels" özelliğini "false" olarak ayarlayarak eksik özet seviyelerini yok sayın,
# ve özet seviyesi 5 başlıklarını seviye 2 olarak değerlendirin.
save_options.outline_options.create_missing_outline_levels = create_missing_outline_levels
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.CreateMissingOutlineLevels.pdf', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [OutlineOptions](../)

