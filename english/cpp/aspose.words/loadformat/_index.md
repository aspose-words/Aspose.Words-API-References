---
title: Aspose::Words::LoadFormat enum
linktitle: LoadFormat
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::LoadFormat enum. Indicates the format of the document that is to be loaded in C++.'
type: docs
weight: 97000
url: /cpp/aspose.words/loadformat/
---
## LoadFormat enum


Indicates the format of the document that is to be loaded.

```cpp
enum class LoadFormat
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Auto | 0 | Instructs Aspose.Words to recognize the format automatically. |
| MsWorks | 8 | Microsoft Works 8 [Document](../document/). |
| Doc | 10 | Microsoft Word 95 or Word 97 - 2003 [Document](../document/). |
| Dot | 11 | Microsoft Word 95 or Word 97 - 2003 Template. |
| DocPreWord60 | 12 | The document is in pre-Word 95 format. Aspose.Words does not currently support loading such documents. |
| Docx | 20 | Office Open XML WordprocessingML [Document](../document/) (macro-free). |
| Docm | 21 | Office Open XML WordprocessingML Macro-Enabled [Document](../document/). |
| Dotx | 22 | Office Open XML WordprocessingML Template (macro-free). |
| Dotm | 23 | Office Open XML WordprocessingML Macro-Enabled Template. |
| FlatOpc | 24 | Office Open XML WordprocessingML stored in a flat XML file instead of a ZIP package. |
| FlatOpcMacroEnabled | 25 | Office Open XML WordprocessingML Macro-Enabled [Document](../document/) stored in a flat XML file instead of a ZIP package. |
| FlatOpcTemplate | 26 | Office Open XML WordprocessingML Template (macro-free) stored in a flat XML file instead of a ZIP package. |
| FlatOpcTemplateMacroEnabled | 27 | Office Open XML WordprocessingML Macro-Enabled Template stored in a flat XML file instead of a ZIP package. |
| Rtf | 30 | RTF format. |
| WordML | 31 | Microsoft Word 2003 WordprocessingML format. |
| Html | 50 | HTML format. |
| Mhtml | 51 | MHTML (Web archive) format. |
| Mobi | 52 | MOBI format. Used by MobiPocket reader and Amazon Kindle readers. |
| Chm | 53 | CHM (Compiled HTML Help) format. |
| Azw3 | 54 | AZW3 format. Used by Amazon Kindle readers. |
| Epub | 55 | EPUB format. |
| Odt | 60 | ODF Text [Document](../document/). |
| Ott | 61 | ODF Text [Document](../document/) Template. |
| Text | 62 | Plain Text. |
| Markdown | 63 | Markdown text document. |
| Xml | 65 | XML document. |
| Unknown | 255 | Unrecognized format, cannot be loaded by [Aspose.Words](../). |


## Examples



Shows how save a web page as a .docx file. 
```cpp
const System::String url = u"https://products.aspose.com/words/";

{
    auto client = System::MakeObject<System::Net::WebClient>();
    auto bytes = client->DownloadData(url);
    {
        auto stream = System::MakeObject<System::IO::MemoryStream>(bytes);
        // The URL is used again as a baseUri to ensure that any relative image paths are retrieved correctly.
        auto options = System::MakeObject<Aspose::Words::Loading::LoadOptions>(Aspose::Words::LoadFormat::Html, u"", url);

        // Load the HTML document from stream and pass the LoadOptions object.
        auto doc = System::MakeObject<Aspose::Words::Document>(stream, options);

        // At this stage, we can read and edit the document's contents and then save it to the local file system.

        doc->Save(get_ArtifactsDir() + u"Document.InsertHtmlFromWebPage.docx");
    }
}
```


Shows how to use the [FileFormatUtil](../fileformatutil/) methods to detect the format of a document. 
```cpp
// Load a document from a file that is missing a file extension, and then detect its file format.
{
    System::SharedPtr<System::IO::FileStream> docStream = System::IO::File::OpenRead(get_MyDir() + u"Word document with missing file extension");
    System::SharedPtr<Aspose::Words::FileFormatInfo> info = Aspose::Words::FileFormatUtil::DetectFileFormat(docStream);
    Aspose::Words::LoadFormat loadFormat = info->get_LoadFormat();

    ASSERT_EQ(Aspose::Words::LoadFormat::Doc, loadFormat);

    // Below are two methods of converting a LoadFormat to its corresponding SaveFormat.
    // 1 -  Get the file extension string for the LoadFormat, then get the corresponding SaveFormat from that string:
    System::String fileExtension = Aspose::Words::FileFormatUtil::LoadFormatToExtension(loadFormat);
    Aspose::Words::SaveFormat saveFormat = Aspose::Words::FileFormatUtil::ExtensionToSaveFormat(fileExtension);

    // 2 -  Convert the LoadFormat directly to its SaveFormat:
    saveFormat = Aspose::Words::FileFormatUtil::LoadFormatToSaveFormat(loadFormat);

    // Load a document from the stream, and then save it to the automatically detected file extension.
    auto doc = System::MakeObject<Aspose::Words::Document>(docStream);

    ASSERT_EQ(u".doc", Aspose::Words::FileFormatUtil::SaveFormatToExtension(saveFormat));

    doc->Save(get_ArtifactsDir() + u"File.SaveToDetectedFileFormat" + Aspose::Words::FileFormatUtil::SaveFormatToExtension(saveFormat));
}
```


Shows how to specify a base URI when opening an html document. 
```cpp
// Suppose we want to load an .html document that contains an image linked by a relative URI
// while the image is in a different location. In that case, we will need to resolve the relative URI into an absolute one.
// We can provide a base URI using an HtmlLoadOptions object.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>(Aspose::Words::LoadFormat::Html, u"", get_ImageDir());

ASSERT_EQ(Aspose::Words::LoadFormat::Html, loadOptions->get_LoadFormat());

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Missing image.html", loadOptions);

// While the image was broken in the input .html, our custom base URI helped us repair the link.
auto imageShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->idx_get(0));
ASSERT_TRUE(imageShape->get_IsImage());

// This output document will display the image that was missing.
doc->Save(get_ArtifactsDir() + u"HtmlLoadOptions.BaseUri.docx");
```

## See Also

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
