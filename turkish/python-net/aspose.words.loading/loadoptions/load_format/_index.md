---
title: LoadOptions.load_format property
linktitle: load_format property
articleTitle: load_format property
second_title: Aspose.Words for Python
description: "LoadOptions.load_format property. Specifies the format of the document to be loaded"
type: docs
weight: 90
url: /tr/python-net/aspose.words.loading/loadoptions/load_format/
---

## LoadOptions.load_format property

Specifies the format of the document to be loaded.
Default is [LoadFormat.AUTO](../../../aspose.words/loadformat/#AUTO).



```python
@property
def load_format(self) -> aspose.words.LoadFormat:
    ...

@load_format.setter
def load_format(self, value: aspose.words.LoadFormat):
    ...

```

### Remarks

It is recommended that you specify the [LoadFormat.AUTO](../../../aspose.words/loadformat/#AUTO) value and let Aspose.Words detect
the file format automatically. If you know the format of the document you are about to load, you can specify the format
explicitly and this will slightly reduce the loading time by the overhead associated with auto detecting the format.
If you specify an explicit load format and it will turn out to be wrong, the auto detection will be invoked and a second
attempt to load the file will be made.




### Examples

Shows how to specify a base URI when opening an html document.

```python
# Bir .html belgesini, göreli bir URI ile bağlanmış bir resmi içeriyorsa yüklemek istediğimizi varsayalım
# Resim farklı bir konumda iken. Bu durumda, göreli URI'yi mutlak bir URI'ye çözmemiz gerekecek.
# Bir HtmlLoadOptions nesnesi kullanarak temel bir URI sağlayabiliriz.
load_options = aw.loading.HtmlLoadOptions(load_format=aw.LoadFormat.HTML, password='', base_uri=IMAGE_DIR)
self.assertEqual(aw.LoadFormat.HTML, load_options.load_format)
doc = aw.Document(file_name=MY_DIR + 'Missing image.html', load_options=load_options)
# Girdi .html dosyasında resim bozukken, özel temel URI'muz bağlantıyı onarmamıza yardımcı oldu.
image_shape = doc.get_child_nodes(aw.NodeType.SHAPE, True)[0].as_shape()
self.assertTrue(image_shape.is_image)
# Bu çıktı belgesi eksik olan resmi gösterecek.
doc.save(file_name=ARTIFACTS_DIR + 'HtmlLoadOptions.BaseUri.docx')
```

### See Also

* module [aspose.words.loading](../../)
* class [LoadOptions](../)

