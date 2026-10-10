---
title: RtfSaveOptions.export_images_for_old_readers property
linktitle: export_images_for_old_readers property
articleTitle: export_images_for_old_readers property
second_title: Aspose.Words for Python
description: "RtfSaveOptions.export_images_for_old_readers property. Specifies whether the keywords for old readers are written to RTF or not"
type: docs
weight: 30
url: /fr/python-net/aspose.words.saving/rtfsaveoptions/export_images_for_old_readers/
---

## RtfSaveOptions.export_images_for_old_readers property

Specifies whether the keywords for "old readers" are written to RTF or not.
This can significantly affect the size of the RTF document.

Default value is ``True``.



```python
@property
def export_images_for_old_readers(self) -> bool:
    ...

@export_images_for_old_readers.setter
def export_images_for_old_readers(self, value: bool):
    ...

```

### Remarks

"Old readers" are pre-Microsoft Word 97 applications and also WordPad.
When this option is ``True`` Aspose.Words writes additional RTF keywords.
These keywords allow the document to be displayed correctly when opened in an 
"old reader" application, but can significantly increase the size of the document.

If you set this option to ``False``, then only images in WMF, EMF and BMP formats
will be displayed in "old readers".




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

