---
title: PdfSaveOptions.outline_options property
linktitle: outline_options property
articleTitle: outline_options property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.outline_options property. Allows to specify outline options."
type: docs
weight: 260
url: /tr/python-net/aspose.words.saving/pdfsaveoptions/outline_options/
---

## PdfSaveOptions.outline_options property

Allows to specify outline options.


```python
@property
def outline_options(self) -> aspose.words.saving.OutlineOptions:
    ...

```

### Remarks

Outlines can be created from headings and bookmarks.

For headings outline level is determined by the heading level.

It is possible to set the max heading level to be included into outlines or disable heading outlines at all.

For bookmarks outline level may be set in options as a default value for all bookmarks or as individual values for particular bookmarks.

Also, outlines can be exported to XPS format by using the same [PdfSaveOptions.outline_options](./) class.




### Examples

Shows how to limit the headings' level that will appear in the outline of a saved PDF document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 1, 2 ve ardından 3 seviyelerinde TOC girdileri olarak hizmet edebilecek başlıklar ekleyin.
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1
self.assertTrue(builder.paragraph_format.is_heading)
builder.writeln('Heading 1')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING2
builder.writeln('Heading 1.1')
builder.writeln('Heading 1.2')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING3
builder.writeln('Heading 1.2.1')
builder.writeln('Heading 1.2.2')
# "PdfSaveOptions" nesnesi oluşturun; bu nesneyi belgenin "Save" metoduna geçebiliriz
# bu yöntemin belgeyi .PDF'ye nasıl dönüştürdüğünü değiştirmek için.
save_options = aw.saving.PdfSaveOptions()
save_options.save_format = aw.SaveFormat.PDF
# Çıktı PDF belgesi bir anahat içerecek; bu, belge gövdesindeki başlıkları listeleyen bir içindekiler tablosudur.
# Bu taslaktaki bir girdiye tıklamak, ilgili başlığın konumuna götürecek.
# "HeadingsOutlineLevels" özelliğini "2" olarak ayarlayarak seviyeleri 2'nin üzerindeki tüm başlıkları taslaktan hariç tutun.
# Yukarıda eklediğimiz son iki başlık görünmeyecek.
save_options.outline_options.headings_outline_levels = 2
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.HeadingsOutlineLevels.pdf', save_options=save_options)
```

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
* class [PdfSaveOptions](../)

