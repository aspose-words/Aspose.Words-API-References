---
title: HtmlSaveOptions.document_split_criteria property
linktitle: document_split_criteria property
articleTitle: document_split_criteria property
second_title: Aspose.Words for Python
description: "HtmlSaveOptions.document_split_criteria property. Specifies how the document should be split when saving to [SaveFormat.HTML](../../../aspose.words/saveformat/#HTML), [SaveFormat.EPUB](../../../aspose.words/saveformat/#EPUB) or [SaveFormat.AZW3](../../../aspose.words/saveformat/#AZW3) format"
type: docs
weight: 80
url: /sv/python-net/aspose.words.saving/htmlsaveoptions/document_split_criteria/
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
# Använd ett SaveOptions-objekt för att ange kodningen för ett dokument som vi ska spara.
save_options = aw.saving.HtmlSaveOptions()
save_options.save_format = aw.SaveFormat.EPUB
save_options.encoding = system_helper.text.Encoding.utf_8()
# Som standard kommer ett genererat .epub-dokument att ha allt innehåll i en HTML-del.
# Ett delningskriterium gör det möjligt att segmentera dokumentet i flera HTML-delar.
# Vi kommer att ställa in kriterierna för att dela dokumentet i rubrikparagrafer.
# Detta är användbart för läsare som inte kan läsa HTML-filer som är större än en viss storlek.
save_options.document_split_criteria = aw.saving.DocumentSplitCriteria.HEADING_PARAGRAPH
# Ange att vi vill exportera dokumentegenskaper.
save_options.export_document_properties = True
doc.save(file_name=ARTIFACTS_DIR + 'HtmlSaveOptions.Doc2EpubSaveOptions.epub', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [HtmlSaveOptions](../)
* property [HtmlSaveOptions.document_split_heading_level](../document_split_heading_level/)
* property [HtmlSaveOptions.document_part_saving_callback](../document_part_saving_callback/)

