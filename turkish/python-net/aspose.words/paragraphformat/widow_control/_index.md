---
title: ParagraphFormat.widow_control property
linktitle: widow_control property
articleTitle: widow_control property
second_title: Aspose.Words for Python
description: "ParagraphFormat.widow_control property. True if the first and last lines in the paragraph are to remain on the same page as the rest of the paragraph."
type: docs
weight: 410
url: /tr/python-net/aspose.words/paragraphformat/widow_control/
---

## ParagraphFormat.widow_control property

True if the first and last lines in the paragraph are to remain on the same page as the rest of the paragraph.


```python
@property
def widow_control(self) -> bool:
    ...

@widow_control.setter
def widow_control(self, value: bool):
    ...

```

### Examples

Shows how to enable widow/orphan control for a paragraph.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Bir sayfaya sığmayan metni yazdığımızda, bir satır bir sonraki sayfaya taşabilir.
# Sonraki sayfada kalan tek satıra "Orphan" (yetim) denir,
# ve yetimin kırıldığı önceki satıra "Widow" (dul) denir.
# Yazı tipini, boşlukları veya sayfa kenar boşluklarını değiştirerek yetimler ve dul satırları düzeltebiliriz.
# Belgemizin boyutlarını korumak istersek, bu bayrağı "true" olarak ayarlayabiliriz
# dul satırları ilgili yetim satırlarıyla aynı sayfaya itmek için.
# Bu bayrağı "false" bırakmak, metinde dul/yetim çiftlerinin kalmasına neden olur.
# Her paragrafın bu ayarı Microsoft Word'de Ana Sayfa -> Paragraf -> Paragraf Ayarları üzerinden erişilebilir
# ("Paragraph" sekmesinin sağ alt köşesindeki düğme) -> "Widow/Orphan control".
builder.paragraph_format.widow_control = widow_control
# Bir yetim ve bir dul üreten metin ekleyin.
builder.font.size = 68
builder.write('Lorem ipsum dolor sit amet, consectetur adipiscing elit, ' + 'sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.')
doc.save(file_name=ARTIFACTS_DIR + 'ParagraphFormat.WidowControl.docx')
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

