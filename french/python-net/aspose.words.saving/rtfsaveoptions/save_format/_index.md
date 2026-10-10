---
title: RtfSaveOptions.save_format property
linktitle: save_format property
articleTitle: save_format property
second_title: Aspose.Words for Python
description: "RtfSaveOptions.save_format property. Specifies the format in which the document will be saved if this save options object is used"
type: docs
weight: 40
url: /fr/python-net/aspose.words.saving/rtfsaveoptions/save_format/
---

## RtfSaveOptions.save_format property

Specifies the format in which the document will be saved if this save options object is used.
Can only be [SaveFormat.RTF](../../../aspose.words/saveformat/#RTF).



```python
@property
def save_format(self) -> aspose.words.SaveFormat:
    ...

@save_format.setter
def save_format(self, value: aspose.words.SaveFormat):
    ...

```

### Examples

Shows how to save a document to .rtf with custom options.

```python
doc = aw.Document(file_name=MY_DIR + 'Rendering.docx')
# Créez un objet "RtfSaveOptions" à transmettre à la méthode "Save" du document afin de modifier la façon dont nous l'enregistrons au format RTF.
options = aw.saving.RtfSaveOptions()
self.assertEqual(aw.SaveFormat.RTF, options.save_format)
# Définissez la propriété "ExportCompactSize" sur "true" pour
# réduire la taille du document enregistré au prix de la compatibilité du texte de droite à gauche.
options.export_compact_size = True
# Définissez la propriété "ExportImagesFotOldReaders" sur "true" pour utiliser des mots-clés supplémentaires afin de garantir que notre document soit
# compatible avec les lecteurs pré-Microsoft Word 97 et WordPad.
# Définissez la propriété "ExportImagesFotOldReaders" sur "false" pour réduire la taille du document,
# mais empêcher les anciens lecteurs de pouvoir lire les images non métafichiers ou BMP que le document pourrait contenir.
options.export_images_for_old_readers = export_images_for_old_readers
doc.save(file_name=ARTIFACTS_DIR + 'RtfSaveOptions.ExportImages.rtf', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [RtfSaveOptions](../)

