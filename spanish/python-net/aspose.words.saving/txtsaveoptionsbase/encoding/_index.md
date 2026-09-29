---
title: TxtSaveOptionsBase.encoding property
linktitle: encoding property
articleTitle: encoding property
second_title: Aspose.Words for Python
description: "TxtSaveOptionsBase.encoding property. Specifies the encoding to use when exporting in text formats"
type: docs
weight: 10
url: /es/python-net/aspose.words.saving/txtsaveoptionsbase/encoding/
---

## TxtSaveOptionsBase.encoding property

Specifies the encoding to use when exporting in text formats. 
Default value is **Encoding.UTF8**.



```python
@property
def encoding(self) -> str:
    ...

@encoding.setter
def encoding(self, value: str):
    ...

```

### Examples

Shows how to set encoding for a .txt output document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Agregue texto con caracteres fuera del conjunto de caracteres ASCII.
builder.write('À È Ì Ò Ù.')
# Cree un objeto "TxtSaveOptions", que podemos pasar al método "Save" del documento
# para modificar cómo guardamos el documento en texto plano.
txt_save_options = aw.saving.TxtSaveOptions()
# Verifique que la propiedad "Encoding" contenga la codificación adecuada para el contenido de nuestro documento.
self.assertEqual(system_helper.text.Encoding.utf_8(), txt_save_options.encoding)
doc.save(file_name=ARTIFACTS_DIR + 'TxtSaveOptions.Encoding.UTF8.txt', save_options=txt_save_options)
doc_text = system_helper.text.Encoding.get_string(system_helper.io.File.read_all_bytes(ARTIFACTS_DIR + 'TxtSaveOptions.Encoding.UTF8.txt'), system_helper.text.Encoding.utf_8())
self.assertEqual('\ufeffÀ È Ì Ò Ù.\r\n', doc_text)
# Usar una codificación inadecuada puede resultar en la pérdida del contenido del documento.
txt_save_options.encoding = system_helper.text.Encoding.ascii()
doc.save(file_name=ARTIFACTS_DIR + 'TxtSaveOptions.Encoding.ASCII.txt', save_options=txt_save_options)
doc_text = system_helper.text.Encoding.get_string(system_helper.io.File.read_all_bytes(ARTIFACTS_DIR + 'TxtSaveOptions.Encoding.ASCII.txt'), system_helper.text.Encoding.ascii())
self.assertEqual('? ? ? ? ?.\r\n', doc_text)
```

### See Also

* module [aspose.words.saving](../../)
* class [TxtSaveOptionsBase](../)

