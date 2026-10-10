---
title: HtmlSaveOptions.export_document_properties property
linktitle: export_document_properties property
articleTitle: export_document_properties property
second_title: Aspose.Words for Python
description: "HtmlSaveOptions.export_document_properties property. Specifies whether to export built-in and custom document properties to HTML, MHTML or EPUB"
type: docs
weight: 120
url: /fr/python-net/aspose.words.saving/htmlsaveoptions/export_document_properties/
---

## HtmlSaveOptions.export_document_properties property

Specifies whether to export built-in and custom document properties to HTML, MHTML or EPUB.
Default value is ``False``.



```python
@property
def export_document_properties(self) -> bool:
    ...

@export_document_properties.setter
def export_document_properties(self, value: bool):
    ...

```

### Examples

Shows how to use a specific encoding when saving a document to .epub.

```python
doc = aw.Document(file_name=MY_DIR + 'Rendering.docx')
# Utilisez un objet SaveOptions pour spécifier l'encodage d'un document que nous allons enregistrer.
save_options = aw.saving.HtmlSaveOptions()
save_options.save_format = aw.SaveFormat.EPUB
save_options.encoding = system_helper.text.Encoding.utf_8()
# Par défaut, un document .epub de sortie contiendra tous ses contenus dans une seule partie HTML.
# Un critère de division nous permet de segmenter le document en plusieurs parties HTML.
# Nous définirons les critères pour diviser le document en paragraphes d'en-tête.
# Ceci est utile pour les lecteurs qui ne peuvent pas lire des fichiers HTML supérieurs à une taille spécifique.
save_options.document_split_criteria = aw.saving.DocumentSplitCriteria.HEADING_PARAGRAPH
# Spécifiez que nous voulons exporter les propriétés du document.
save_options.export_document_properties = True
doc.save(file_name=ARTIFACTS_DIR + 'HtmlSaveOptions.Doc2EpubSaveOptions.epub', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [HtmlSaveOptions](../)

