---
title: LoadFormat Enum
linktitle: LoadFormat
articleTitle: LoadFormat
second_title: Aspose.Words for .NET
description: Aspose.Words.LoadFormat enum. Indicates the format of the document that is to be loaded in C#.
type: docs
weight: 3970
url: /net/aspose.words/loadformat/
---
## LoadFormat enumeration

Indicates the format of the document that is to be loaded.

```csharp
public enum LoadFormat
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Auto | `0` | Instructs Aspose.Words to recognize the format automatically. |
| Doc | `10` | Microsoft Word 95 or Word 97 - 2003 Document. |
| Dot | `11` | Microsoft Word 95 or Word 97 - 2003 Template. |
| DocPreWord60 | `12` | The document is in pre-Word 95 format. Aspose.Words does not currently support loading such documents. |
| Docx | `20` | Office Open XML WordprocessingML Document (macro-free). |
| Docm | `21` | Office Open XML WordprocessingML Macro-Enabled Document. |
| Dotx | `22` | Office Open XML WordprocessingML Template (macro-free). |
| Dotm | `23` | Office Open XML WordprocessingML Macro-Enabled Template. |
| FlatOpc | `24` | Office Open XML WordprocessingML stored in a flat XML file instead of a ZIP package. |
| FlatOpcMacroEnabled | `25` | Office Open XML WordprocessingML Macro-Enabled Document stored in a flat XML file instead of a ZIP package. |
| FlatOpcTemplate | `26` | Office Open XML WordprocessingML Template (macro-free) stored in a flat XML file instead of a ZIP package. |
| FlatOpcTemplateMacroEnabled | `27` | Office Open XML WordprocessingML Macro-Enabled Template stored in a flat XML file instead of a ZIP package. |
| Rtf | `30` | RTF format. |
| WordML | `31` | Microsoft Word 2003 WordprocessingML format. |
| Html | `50` | HTML format. |
| Mhtml | `51` | MHTML (Web archive) format. |
| Mobi | `52` | MOBI format. Used by MobiPocket reader and Amazon Kindle readers. |
| Chm | `53` | CHM (Compiled HTML Help) format. |
| Azw3 | `54` | AZW3 format. Used by Amazon Kindle readers. |
| Epub | `55` | EPUB format. |
| Odt | `60` | ODF Text Document. |
| Ott | `61` | ODF Text Document Template. |
| Text | `62` | Plain Text. |
| Markdown | `63` | Markdown text document. |
| Pdf | `64` | Pdf document. |
| Xml | `65` | XML document. |
| Unknown | `255` | Unrecognized format, cannot be loaded by Aspose.Words. |

## Examples

Shows how save a web page as a .docx file.

```csharp
const string url = "https://products.aspose.com/words/";

using (WebClient client = new WebClient())
{
    var bytes = client.DownloadData(url);
    using (MemoryStream stream = new MemoryStream(bytes))
    {
        // The URL is used again as a baseUri to ensure that any relative image paths are retrieved correctly.
        LoadOptions options = new LoadOptions(LoadFormat.Html, "", url);

        // Load the HTML document from stream and pass the LoadOptions object.
        Document doc = new Document(stream, options);

        // At this stage, we can read and edit the document's contents and then save it to the local file system.
        doc.Save(ArtifactsDir + "Document.InsertHtmlFromWebPage.docx");
    }
}
```

Shows how to specify a base URI when opening an html document.

```csharp
// Suppose we want to load an .html document that contains an image linked by a relative URI
// while the image is in a different location. In that case, we will need to resolve the relative URI into an absolute one.
// We can provide a base URI using an HtmlLoadOptions object. 
HtmlLoadOptions loadOptions = new HtmlLoadOptions(LoadFormat.Html, "", ImageDir);

Assert.AreEqual(LoadFormat.Html, loadOptions.LoadFormat);

Document doc = new Document(MyDir + "Missing image.html", loadOptions);

// While the image was broken in the input .html, our custom base URI helped us repair the link.
Shape imageShape = (Shape)doc.GetChildNodes(NodeType.Shape, true)[0];
Assert.True(imageShape.IsImage);

// This output document will display the image that was missing.
doc.Save(ArtifactsDir + "HtmlLoadOptions.BaseUri.docx");
```

Shows how to use the FileFormatUtil methods to detect the format of a document.

```csharp
// Load a document from a file that is missing a file extension, and then detect its file format.
using (FileStream docStream = File.OpenRead(MyDir + "Word document with missing file extension"))
{
    FileFormatInfo info = FileFormatUtil.DetectFileFormat(docStream);
    LoadFormat loadFormat = info.LoadFormat;

    Assert.AreEqual(LoadFormat.Doc, loadFormat);

    // Below are two methods of converting a LoadFormat to its corresponding SaveFormat.
    // 1 -  Get the file extension string for the LoadFormat, then get the corresponding SaveFormat from that string:
    string fileExtension = FileFormatUtil.LoadFormatToExtension(loadFormat);
    SaveFormat saveFormat = FileFormatUtil.ExtensionToSaveFormat(fileExtension);

    // 2 -  Convert the LoadFormat directly to its SaveFormat:
    saveFormat = FileFormatUtil.LoadFormatToSaveFormat(loadFormat);

    // Load a document from the stream, and then save it to the automatically detected file extension.
    Document doc = new Document(docStream);

    Assert.AreEqual(".doc", FileFormatUtil.SaveFormatToExtension(saveFormat));

    doc.Save(ArtifactsDir + "File.SaveToDetectedFileFormat" + FileFormatUtil.SaveFormatToExtension(saveFormat));
}
```

### See Also

* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
