---
title: TxtSaveOptionsBase.encoding property
linktitle: encoding property
articleTitle: encoding property
second_title: Aspose.Words for Python
description: "TxtSaveOptionsBase.encoding property. Specifies the encoding to use when exporting in text formats"
type: docs
weight: 10
url: /fr/python-net/aspose.words.saving/txtsaveoptionsbase/encoding/
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
# Ajoutez du texte contenant des caractères hors du jeu de caractères ASCII.
builder.write('À È Ì Ò Ù.')
# Créez un objet "TxtSaveOptions", que nous pouvons transmettre à la méthode "Save" du document
# pour modifier la façon dont nous enregistrons le document en texte brut.
txt_save_options = aw.saving.TxtSaveOptions()
# Vérifiez que la propriété "Encoding" contient le codage approprié pour le contenu de notre document.
self.assertEqual(system_helper.text.Encoding.utf_8(), txt_save_options.encoding)
doc.save(file_name=ARTIFACTS_DIR + 'TxtSaveOptions.Encoding.UTF8.txt', save_options=txt_save_options)
doc_text = system_helper.text.Encoding.get_string(system_helper.io.File.read_all_bytes(ARTIFACTS_DIR + 'TxtSaveOptions.Encoding.UTF8.txt'), system_helper.text.Encoding.utf_8())
self.assertEqual('\ufeffÀ È Ì Ò Ù.\r\n', doc_text)
# Utiliser un codage inapproprié peut entraîner une perte du contenu du document.
txt_save_options.encoding = system_helper.text.Encoding.ascii()
doc.save(file_name=ARTIFACTS_DIR + 'TxtSaveOptions.Encoding.ASCII.txt', save_options=txt_save_options)
doc_text = system_helper.text.Encoding.get_string(system_helper.io.File.read_all_bytes(ARTIFACTS_DIR + 'TxtSaveOptions.Encoding.ASCII.txt'), system_helper.text.Encoding.ascii())
self.assertEqual('? ? ? ? ?.\r\n', doc_text)
```

### See Also

* module [aspose.words.saving](../../)
* class [TxtSaveOptionsBase](../)

