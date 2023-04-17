---
title: Aspose::Words::FileFormatUtil::LoadFormatToExtension method
linktitle: LoadFormatToExtension
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::FileFormatUtil::LoadFormatToExtension method. Converts a load format enumerated value into a file extension. The returned extension is a lower-case string with a leading dot in C++.'
type: docs
weight: 6000
url: /cpp/aspose.words/fileformatutil/loadformattoextension/
---
## FileFormatUtil::LoadFormatToExtension method


Converts a load format enumerated value into a file extension. The returned extension is a lower-case string with a leading dot.

```cpp
static System::String Aspose::Words::FileFormatUtil::LoadFormatToExtension(Aspose::Words::LoadFormat loadFormat)
```

## Remarks


The [WordML](../../saveformat/) value is converted to ".wml".

## Examples



Shows how to use the [FileFormatUtil](../) methods to detect the format of a document. 
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

* Enum [LoadFormat](../../loadformat/)
* Class [FileFormatUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
