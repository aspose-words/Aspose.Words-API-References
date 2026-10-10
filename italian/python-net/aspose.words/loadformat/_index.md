---
title: LoadFormat enumeration
linktitle: LoadFormat enumeration
articleTitle: LoadFormat enumeration
second_title: Aspose.Words for Python
description: "aspose.words.LoadFormat enumeration. Indicates the format of the document that is to be loaded."
type: docs
weight: 750
url: /it/python-net/aspose.words/loadformat/
---

## LoadFormat enumeration

Indicates the format of the document that is to be loaded.


### Members

| Name | Description |
| --- | --- |
| AUTO | Instructs Aspose.Words to recognize the format automatically. |
| MS_WORKS | Microsoft Works 8 Document. |
| DOC | Microsoft Word 95 or Word 97 - 2003 Document. |
| DOT | Microsoft Word 95 or Word 97 - 2003 Template. |
| DOC_PRE_WORD60 | The document is in pre-Word 95 format. Aspose.Words does not currently support loading such documents. |
| DOCX | Office Open XML WordprocessingML Document (macro-free). |
| DOCM | Office Open XML WordprocessingML Macro-Enabled Document. |
| DOTX | Office Open XML WordprocessingML Template (macro-free). |
| DOTM | Office Open XML WordprocessingML Macro-Enabled Template. |
| FLAT_OPC | Office Open XML WordprocessingML stored in a flat XML file instead of a ZIP package. |
| FLAT_OPC_MACRO_ENABLED | Office Open XML WordprocessingML Macro-Enabled Document stored in a flat XML file instead of a ZIP package. |
| FLAT_OPC_TEMPLATE | Office Open XML WordprocessingML Template (macro-free) stored in a flat XML file instead of a ZIP package. |
| FLAT_OPC_TEMPLATE_MACRO_ENABLED | Office Open XML WordprocessingML Macro-Enabled Template stored in a flat XML file instead of a ZIP package. |
| RTF | RTF format. |
| WORD_ML | Microsoft Word 2003 WordprocessingML format. |
| HTML | HTML format. |
| MHTML | MHTML (Web archive) format. |
| MOBI | MOBI format. Used by MobiPocket reader and Amazon Kindle readers. |
| CHM | CHM (Compiled HTML Help) format. |
| AZW3 | AZW3 format. Used by Amazon Kindle readers. |
| EPUB | EPUB format. |
| ODT | ODF Text Document. |
| OTT | ODF Text Document Template. |
| TEXT | Plain Text. |
| MARKDOWN | Markdown text document. |
| PDF | Pdf document. |
| XML | XML document. |
| UNKNOWN | Unrecognized format, cannot be loaded by Aspose.Words. |

### Examples

Shows how to use the FileFormatUtil methods to detect the format of a document.

```python
# Carica un documento da un file privo di estensione e poi rileva il suo formato.
with system_helper.io.File.open_read(MY_DIR + 'Word document with missing file extension') as doc_stream:
    info = aw.FileFormatUtil.detect_file_format(stream=doc_stream)
    load_format = info.load_format
    self.assertEqual(aw.LoadFormat.DOC, load_format)
    # Di seguito sono riportati due metodi per convertire un LoadFormat nel relativo SaveFormat.
    # 1 -  Ottieni la stringa dell'estensione file per il LoadFormat, quindi ottieni il SaveFormat corrispondente da quella stringa:
    file_extension = aw.FileFormatUtil.load_format_to_extension(load_format)
    save_format = aw.FileFormatUtil.extension_to_save_format(file_extension)
    # 2 -  Converti direttamente il LoadFormat nel suo SaveFormat:
    save_format = aw.FileFormatUtil.load_format_to_save_format(load_format)
    # Carica un documento dallo stream, quindi salvalo con l'estensione file rilevata automaticamente.
    doc = aw.Document(stream=doc_stream)
    self.assertEqual('.doc', aw.FileFormatUtil.save_format_to_extension(save_format))
    doc.save(file_name=ARTIFACTS_DIR + 'File.SaveToDetectedFileFormat' + aw.FileFormatUtil.save_format_to_extension(save_format))
```

Shows how to specify a base URI when opening an html document.

```python
# Supponiamo di voler caricare un documento .html che contiene un'immagine collegata tramite un URI relativo
# mentre l'immagine si trova in una posizione diversa. In tal caso, dovremo risolvere l'URI relativo in uno assoluto.
# Possiamo fornire un URI di base usando un oggetto HtmlLoadOptions.
load_options = aw.loading.HtmlLoadOptions(load_format=aw.LoadFormat.HTML, password='', base_uri=IMAGE_DIR)
self.assertEqual(aw.LoadFormat.HTML, load_options.load_format)
doc = aw.Document(file_name=MY_DIR + 'Missing image.html', load_options=load_options)
# Anche se l'immagine era interrotta nell'.html di input, il nostro URI di base personalizzato ci ha aiutato a riparare il collegamento.
image_shape = doc.get_child_nodes(aw.NodeType.SHAPE, True)[0].as_shape()
self.assertTrue(image_shape.is_image)
# Questo documento di output mostrerà l'immagine che mancava.
doc.save(file_name=ARTIFACTS_DIR + 'HtmlLoadOptions.BaseUri.docx')
```

### See Also

* module [aspose.words](../)

