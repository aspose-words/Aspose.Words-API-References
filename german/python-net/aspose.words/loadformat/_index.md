---
title: LoadFormat enumeration
linktitle: LoadFormat enumeration
articleTitle: LoadFormat enumeration
second_title: Aspose.Words for Python
description: "aspose.words.LoadFormat enumeration. Indicates the format of the document that is to be loaded."
type: docs
weight: 750
url: /de/python-net/aspose.words/loadformat/
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
# Laden Sie ein Dokument aus einer Datei, der eine Dateierweiterung fehlt, und erkennen Sie anschließend ihr Dateiformat.
with system_helper.io.File.open_read(MY_DIR + 'Word document with missing file extension') as doc_stream:
    info = aw.FileFormatUtil.detect_file_format(stream=doc_stream)
    load_format = info.load_format
    self.assertEqual(aw.LoadFormat.DOC, load_format)
    # Unten sind zwei Methoden aufgeführt, um ein LoadFormat in das entsprechende SaveFormat zu konvertieren.
    # 1 -  Holen Sie die Dateierweiterungszeichenkette für das LoadFormat und erhalten Sie dann das entsprechende SaveFormat aus dieser Zeichenkette:
    file_extension = aw.FileFormatUtil.load_format_to_extension(load_format)
    save_format = aw.FileFormatUtil.extension_to_save_format(file_extension)
    # 2 -  Konvertieren Sie das LoadFormat direkt in sein SaveFormat:
    save_format = aw.FileFormatUtil.load_format_to_save_format(load_format)
    # Laden Sie ein Dokument aus dem Stream und speichern Sie es anschließend mit der automatisch erkannten Dateierweiterung.
    doc = aw.Document(stream=doc_stream)
    self.assertEqual('.doc', aw.FileFormatUtil.save_format_to_extension(save_format))
    doc.save(file_name=ARTIFACTS_DIR + 'File.SaveToDetectedFileFormat' + aw.FileFormatUtil.save_format_to_extension(save_format))
```

Shows how to specify a base URI when opening an html document.

```python
# Angenommen, wir möchten ein .html-Dokument laden, das ein Bild enthält, das über einen relativen URI verlinkt ist
# während sich das Bild an einem anderen Ort befindet. In diesem Fall müssen wir den relativen URI in einen absoluten URI auflösen.
# Wir können mithilfe eines HtmlLoadOptions-Objekts eine Basis-URI bereitstellen.
load_options = aw.loading.HtmlLoadOptions(load_format=aw.LoadFormat.HTML, password='', base_uri=IMAGE_DIR)
self.assertEqual(aw.LoadFormat.HTML, load_options.load_format)
doc = aw.Document(file_name=MY_DIR + 'Missing image.html', load_options=load_options)
# Obwohl das Bild im Eingabe-.html beschädigt war, hat unsere benutzerdefinierte Basis-URI uns geholfen, den Link zu reparieren.
image_shape = doc.get_child_nodes(aw.NodeType.SHAPE, True)[0].as_shape()
self.assertTrue(image_shape.is_image)
# Dieses Ausgabedokument wird das fehlende Bild anzeigen.
doc.save(file_name=ARTIFACTS_DIR + 'HtmlLoadOptions.BaseUri.docx')
```

### See Also

* module [aspose.words](../)

