---
title: LoadFormat enumeration
linktitle: LoadFormat enumeration
articleTitle: LoadFormat enumeration
second_title: Aspose.Words for Python
description: "aspose.words.LoadFormat enumeration. Indicates the format of the document that is to be loaded."
type: docs
weight: 750
url: /es/python-net/aspose.words/loadformat/
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
# Cargue un documento desde un archivo que carece de extensión y luego detecte su formato de archivo.
with system_helper.io.File.open_read(MY_DIR + 'Word document with missing file extension') as doc_stream:
    info = aw.FileFormatUtil.detect_file_format(stream=doc_stream)
    load_format = info.load_format
    self.assertEqual(aw.LoadFormat.DOC, load_format)
    # A continuación se presentan dos métodos para convertir un LoadFormat a su correspondiente SaveFormat.
    # 1 -  Obtenga la cadena de extensión de archivo para el LoadFormat, luego obtenga el SaveFormat correspondiente a partir de esa cadena:
    file_extension = aw.FileFormatUtil.load_format_to_extension(load_format)
    save_format = aw.FileFormatUtil.extension_to_save_format(file_extension)
    # 2 -  Convierta el LoadFormat directamente a su SaveFormat:
    save_format = aw.FileFormatUtil.load_format_to_save_format(load_format)
    # Cargue un documento desde el flujo y luego guárdelo con la extensión de archivo detectada automáticamente.
    doc = aw.Document(stream=doc_stream)
    self.assertEqual('.doc', aw.FileFormatUtil.save_format_to_extension(save_format))
    doc.save(file_name=ARTIFACTS_DIR + 'File.SaveToDetectedFileFormat' + aw.FileFormatUtil.save_format_to_extension(save_format))
```

Shows how to specify a base URI when opening an html document.

```python
# Supongamos que queremos cargar un documento .html que contiene una imagen vinculada mediante una URI relativa
# mientras que la imagen está en una ubicación diferente. En ese caso, necesitaremos resolver la URI relativa en una absoluta.
# Podemos proporcionar una URI base usando un objeto HtmlLoadOptions.
load_options = aw.loading.HtmlLoadOptions(load_format=aw.LoadFormat.HTML, password='', base_uri=IMAGE_DIR)
self.assertEqual(aw.LoadFormat.HTML, load_options.load_format)
doc = aw.Document(file_name=MY_DIR + 'Missing image.html', load_options=load_options)
# Aunque la imagen estaba rota en el .html de entrada, nuestra URI base personalizada nos ayudó a reparar el enlace.
image_shape = doc.get_child_nodes(aw.NodeType.SHAPE, True)[0].as_shape()
self.assertTrue(image_shape.is_image)
# Este documento de salida mostrará la imagen que faltaba.
doc.save(file_name=ARTIFACTS_DIR + 'HtmlLoadOptions.BaseUri.docx')
```

### See Also

* module [aspose.words](../)

