---
title: HtmlSaveOptions.document_split_criteria property
linktitle: document_split_criteria property
articleTitle: document_split_criteria property
second_title: Aspose.Words for Python
description: "HtmlSaveOptions.document_split_criteria property. Specifies how the document should be split when saving to [SaveFormat.HTML](../../../aspose.words/saveformat/#HTML), [SaveFormat.EPUB](../../../aspose.words/saveformat/#EPUB) or [SaveFormat.AZW3](../../../aspose.words/saveformat/#AZW3) format"
type: docs
weight: 80
url: /fr/python-net/aspose.words.saving/htmlsaveoptions/document_split_criteria/
---

## HtmlSaveOptions.document_split_criteria property

Specifies how the document should be split when saving to [SaveFormat.HTML](../../../aspose.words/saveformat/#HTML),
[SaveFormat.EPUB](../../../aspose.words/saveformat/#EPUB) or [SaveFormat.AZW3](../../../aspose.words/saveformat/#AZW3) format.
Default is [DocumentSplitCriteria.NONE](../../documentsplitcriteria/#NONE) for HTML and
[DocumentSplitCriteria.HEADING_PARAGRAPH](../../documentsplitcriteria/#HEADING_PARAGRAPH) for EPUB and AZW3.



```python
@property
def document_split_criteria(self) -> aspose.words.saving.DocumentSplitCriteria:
    ...

@document_split_criteria.setter
def document_split_criteria(self, value: aspose.words.saving.DocumentSplitCriteria):
    ...

```

### Remarks

Normally you would want a document saved to HTML as a single file.
But in some cases it is preferable to split the output into several smaller HTML pages.
When saving to HTML format these pages will be output to individual files or streams.
When saving to EPUB format they will be incorporated into corresponding packages.

A document cannot be split when saving in the MHTML format.




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
* property [HtmlSaveOptions.document_split_heading_level](../document_split_heading_level/)
* property [HtmlSaveOptions.document_part_saving_callback](../document_part_saving_callback/)

