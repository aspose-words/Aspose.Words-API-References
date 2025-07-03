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

## See Also

* Enum [LoadFormat](../../loadformat/)
* Class [FileFormatUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
