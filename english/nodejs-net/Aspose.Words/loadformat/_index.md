---
title: LoadFormat enumeration
linktitle: LoadFormat enumeration
articleTitle: LoadFormat enumeration
second_title: Aspose.Words for Node.js
description: "Aspose.Words.LoadFormat enumeration. Indicates the format of the document that is to be loaded."
type: docs
weight: 800
url: /nodejs-net/aspose.words/loadformat/
---

## LoadFormat enumeration

Indicates the format of the document that is to be loaded.


### Members

| Name | Description |
| --- | --- |
| Auto | Instructs Aspose.Words to recognize the format automatically. |
| MsWorks | Microsoft Works 8 Document. |
| Doc | Microsoft Word 95 or Word 97 - 2003 Document. |
| Dot | Microsoft Word 95 or Word 97 - 2003 Template. |
| DocPreWord60 | The document is in pre-Word 95 format. Aspose.Words does not currently support loading such documents. |
| Docx | Office Open XML WordprocessingML Document (macro-free). |
| Docm | Office Open XML WordprocessingML Macro-Enabled Document. |
| Dotx | Office Open XML WordprocessingML Template (macro-free). |
| Dotm | Office Open XML WordprocessingML Macro-Enabled Template. |
| FlatOpc | Office Open XML WordprocessingML stored in a flat XML file instead of a ZIP package. |
| FlatOpcMacroEnabled | Office Open XML WordprocessingML Macro-Enabled Document stored in a flat XML file instead of a ZIP package. |
| FlatOpcTemplate | Office Open XML WordprocessingML Template (macro-free) stored in a flat XML file instead of a ZIP package. |
| FlatOpcTemplateMacroEnabled | Office Open XML WordprocessingML Macro-Enabled Template stored in a flat XML file instead of a ZIP package. |
| Rtf | RTF format. |
| WordML | Microsoft Word 2003 WordprocessingML format. |
| Html | HTML format. |
| Mhtml | MHTML (Web archive) format. |
| Mobi | MOBI format. Used by MobiPocket reader and Amazon Kindle readers. |
| Chm | CHM (Compiled HTML Help) format. |
| Azw3 | AZW3 format. Used by Amazon Kindle readers. |
| Epub | EPUB format. |
| Odt | ODF Text Document. |
| Ott | ODF Text Document Template. |
| Text | Plain Text. |
| Markdown | Markdown text document. |
| Pdf | Pdf document. |
| Xml | XML document. |
| Unknown | Unrecognized format, cannot be loaded by Aspose.Words. |

### Examples

Shows how to use the FileFormatUtil methods to detect the format of a document.

```js
// Load a document from a file that is missing a file extension, and then detect its file format.
let docStream = base.loadFileToBuffer(base.myDir + "Word document with missing file extension");
let info = aw.FileFormatUtil.detectFileFormat(docStream);
let loadFormat = info.loadFormat;
expect(loadFormat).toEqual(aw.LoadFormat.Doc);
// Below are two methods of converting a LoadFormat to its corresponding SaveFormat.
// 1 -  Get the file extension string for the LoadFormat, then get the corresponding SaveFormat from that string:
let fileExtension = aw.FileFormatUtil.loadFormatToExtension(loadFormat);
let saveFormat = aw.FileFormatUtil.extensionToSaveFormat(fileExtension);
// 2 -  Convert the LoadFormat directly to its SaveFormat:
saveFormat = aw.FileFormatUtil.loadFormatToSaveFormat(loadFormat);
// Load a document from the stream, and then save it to the automatically detected file extension.
let doc = new aw.Document(docStream);
expect(aw.FileFormatUtil.saveFormatToExtension(saveFormat)).toEqual(".doc");
doc.save(base.artifactsDir + "File.SaveToDetectedFileFormat" + aw.FileFormatUtil.saveFormatToExtension(saveFormat));
```

Shows how save a web page as a .docx file.

```js
const url = "https://products.aspose.com/words/";
const response = await fetch(url);
const blob = await response.blob();
const arrayBuffer = await blob.arrayBuffer();
const dataBytes = Buffer.from(arrayBuffer);    

let doc = new aw.Document(dataBytes);

// At this stage, we can read and edit the document's contents and then save it to the local file system.

doc.save(base.artifactsDir + "Document.LoadFromWeb.docx");
```

### See Also

* module [Aspose.Words](../)

