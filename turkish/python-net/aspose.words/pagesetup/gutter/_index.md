---
title: PageSetup.gutter property
linktitle: gutter property
articleTitle: gutter property
second_title: Aspose.Words for Python
description: "PageSetup.gutter property. Gets or sets the amount of extra space added to the margin for document binding."
type: docs
weight: 160
url: /tr/python-net/aspose.words/pagesetup/gutter/
---

## PageSetup.gutter property

Gets or sets the amount of extra space added to the margin for document binding.


```python
@property
def gutter(self) -> float:
    ...

@gutter.setter
def gutter(self, value: float):
    ...

```

### Examples

Shows how to set gutter margins.

```python
doc = aw.Document()
# Birden fazla sayfayı kapsayan metin ekleyin.
builder = aw.DocumentBuilder(doc=doc)
i = 0
while i < 6:
    builder.write('Lorem ipsum dolor sit amet, consectetur adipiscing elit, ' + 'sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.')
    builder.insert_break(aw.BreakType.PAGE_BREAK)
    i += 1
# Bir oluk, sayfanın sol ya da sağ kenar boşluğuna boşluk ekler,
# bu, bir kitabın ortadaki katlanmasının sayfa düzenine müdahalesini telafi eder.
page_setup = doc.sections[0].page_setup
# Sayfalarımızın kenar boşlukları içinde metin için ne kadar alanı olduğunu belirleyin ve ardından bir kenar boşluğunu doldurmak için bir miktar ekleyin.
self.assertAlmostEqual(470.3, page_setup.page_width - page_setup.left_margin - page_setup.right_margin, delta=0.01)
page_setup.gutter = 100
# "RtlGutter" özelliğini "true" olarak ayarlayarak, oluk sağdan sola metin için daha uygun bir konuma yerleştirin.
page_setup.rtl_gutter = True
# "MultiplePages" özelliğini "MultiplePagesType.MirrorMargins" olarak ayarlayarak değiştirmek için
# her sayfada kenar boşluklarının sol/sağ sayfa tarafı konumunu.
page_setup.multiple_pages = aw.settings.MultiplePagesType.MIRROR_MARGINS
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.Gutter.docx')
```

Shows how to configure a document that can be printed as a book fold.

```python
doc = aw.Document()
# 16 sayfayı kapsayan metin ekleyin.
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('My Booklet:')
i = 0
while i < 15:
    builder.insert_break(aw.BreakType.PAGE_BREAK)
    builder.write(f'Booklet face #{i}')
    i += 1
# İlk bölümün "PageSetup" özelliğini belgenin kitap katlaması şeklinde yazdıracak şekilde yapılandırın.
# Bu belgeyi çift taraflı yazdırdığımızda, sayfaları alıp yığabiliriz
# ve hepsini bir anda ortasından katlayın. Belgenin içeriği bir kitap katlaması şeklinde hizalanacaktır.
page_setup = doc.sections[0].page_setup
page_setup.multiple_pages = aw.settings.MultiplePagesType.BOOK_FOLD_PRINTING
# Yalnızca sayfa sayısını 4'ün katları olarak belirtebiliriz.
page_setup.sheets_per_booklet = 4
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.Booklet.docx')
```

### See Also

* module [aspose.words](../../)
* class [PageSetup](../)

