---
title: SaveOptions.save_format property
linktitle: save_format property
articleTitle: save_format property
second_title: Aspose.Words for Python
description: "SaveOptions.save_format property. Specifies the format in which the document will be saved if this save options object is used."
type: docs
weight: 110
url: /tr/python-net/aspose.words.saving/saveoptions/save_format/
---

## SaveOptions.save_format property

Specifies the format in which the document will be saved if this save options object is used.


```python
@property
def save_format(self) -> aspose.words.SaveFormat:
    ...

@save_format.setter
def save_format(self, value: aspose.words.SaveFormat):
    ...

```

### Examples

Shows how to use a specific encoding when saving a document to .epub.

```python
doc = aw.Document(file_name=MY_DIR + 'Rendering.docx')
# Kaydedeceğimiz belge için kodlamayı belirtmek üzere bir SaveOptions nesnesi kullanın.
save_options = aw.saving.HtmlSaveOptions()
save_options.save_format = aw.SaveFormat.EPUB
save_options.encoding = system_helper.text.Encoding.utf_8()
# Varsayılan olarak, bir çıktı .epub belgesi tüm içeriğini tek bir HTML bölümünde tutar.
# Bir bölme ölçütü, belgeyi birden fazla HTML bölümüne ayırmamıza olanak tanır.
# Belgeyi başlık paragraflarına bölmek için ölçütleri ayarlayacağız.
# Bu, belirli bir boyuttan daha büyük HTML dosyalarını okuyamayan okuyucular için faydalıdır.
save_options.document_split_criteria = aw.saving.DocumentSplitCriteria.HEADING_PARAGRAPH
# Belge özelliklerini dışa aktarmak istediğimizi belirtin.
save_options.export_document_properties = True
doc.save(file_name=ARTIFACTS_DIR + 'HtmlSaveOptions.Doc2EpubSaveOptions.epub', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [SaveOptions](../)

