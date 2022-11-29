---
title: get_OriginalFileName
second_title: Aspose.Words for C++ API Reference
description: Gets the original file name of the document.
type: docs
weight: 469
url: /cpp/aspose.words/document/get_originalfilename/
---
## Document::get_OriginalFileName method


Gets the original file name of the document.

```cpp
System::String Aspose::Words::Document::get_OriginalFileName() const
```

## Remarks


Returns null if the document was loaded from a stream or created blank.

## Examples



Shows how to retrieve details of a document's load operation. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Document.docx");

ASSERT_EQ(MyDir + u"Document.docx", doc->get_OriginalFileName());
ASSERT_EQ(LoadFormat::Docx, doc->get_OriginalLoadFormat());
```


Shows how to use the [FileFormatUtil](../../fileformatutil/) methods to detect the format of a document. 
```cpp
// Load a document from a file that is missing a file extension, and then detect its file format.
{
    SharedPtr<System::IO::FileStream> docStream = System::IO::File::OpenRead(MyDir + u"Word document with missing file extension");
    SharedPtr<FileFormatInfo> info = FileFormatUtil::DetectFileFormat(docStream);
    LoadFormat loadFormat = info->get_LoadFormat();

    ASSERT_EQ(LoadFormat::Doc, loadFormat);

    // Below are two methods of converting a LoadFormat to its corresponding SaveFormat.
    // 1 -  Get the file extension string for the LoadFormat, then get the corresponding SaveFormat from that string:
    String fileExtension = FileFormatUtil::LoadFormatToExtension(loadFormat);
    SaveFormat saveFormat = FileFormatUtil::ExtensionToSaveFormat(fileExtension);

    // 2 -  Convert the LoadFormat directly to its SaveFormat:
    saveFormat = FileFormatUtil::LoadFormatToSaveFormat(loadFormat);

    // Load a document from the stream, and then save it to the automatically detected file extension.
    auto doc = MakeObject<Document>(docStream);

    ASSERT_EQ(u".doc", FileFormatUtil::SaveFormatToExtension(saveFormat));

    doc->Save(ArtifactsDir + u"File.SaveToDetectedFileFormat" + FileFormatUtil::SaveFormatToExtension(saveFormat));
}
```

## See Also

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
