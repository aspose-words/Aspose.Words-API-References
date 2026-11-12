---
title: XpsSaveOptions.save_format property
linktitle: save_format property
articleTitle: save_format property
second_title: Aspose.Words for Python
description: "XpsSaveOptions.save_format property. Specifies the format in which the document will be saved if this save options object is used"
type: docs
weight: 50
url: /tr/python-net/aspose.words.saving/xpssaveoptions/save_format/
---

## XpsSaveOptions.save_format property

Specifies the format in which the document will be saved if this save options object is used.
Can only be [SaveFormat.XPS](../../../aspose.words/saveformat/#XPS).



```python
@property
def save_format(self) -> aspose.words.SaveFormat:
    ...

@save_format.setter
def save_format(self, value: aspose.words.SaveFormat):
    ...

```

### Examples

Shows how to limit the headings' level that will appear in the outline of a saved XPS document.

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
# "XpsSaveOptions" nesnesi oluşturun ve bunu belgenin "Save" metoduna geçirebiliriz
# bu metodun belgeyi .XPS'e nasıl dönüştürdüğünü değiştirmek için.
save_options = aw.saving.XpsSaveOptions()
self.assertEqual(aw.SaveFormat.XPS, save_options.save_format)
# Çıktı XPS belgesi, belge gövdesindeki başlıkları listeleyen bir taslak, içindekiler tablosu içerecek.
# Bu taslaktaki bir girdiye tıklamak, ilgili başlığın konumuna götürecek.
# "HeadingsOutlineLevels" özelliğini "2" olarak ayarlayarak seviyeleri 2'nin üzerindeki tüm başlıkları taslaktan hariç tutun.
# Yukarıda eklediğimiz son iki başlık görünmeyecek.
save_options.outline_options.headings_outline_levels = 2
doc.save(file_name=ARTIFACTS_DIR + 'XpsSaveOptions.OutlineLevels.xps', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [XpsSaveOptions](../)

