---
title: Aspose::Words::FileFormatUtil class
linktitle: FileFormatUtil
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::FileFormatUtil class. Provides utility methods for working with file formats, such as detecting file format or converting file extensions to/from file format enums. To learn more, visit the  documentation article in C++.'
type: docs
weight: 28000
url: /cpp/aspose.words/fileformatutil/
---
## FileFormatUtil class


Provides utility methods for working with file formats, such as detecting file format or converting file extensions to/from file format enums. To learn more, visit the [Detect File Format and Check Format Compatibility](https://docs.aspose.com/words/cpp/detect-file-format-and-check-format-compatibility/) documentation article.

```cpp
class FileFormatUtil
```

## Methods

| Method | Description |
| --- | --- |
| static [ContentTypeToLoadFormat](./contenttypetoloadformat/)(const System::String\&) | Converts IANA content type into a load format enumerated value. |
| static [ContentTypeToSaveFormat](./contenttypetosaveformat/)(const System::String\&) | Converts IANA content type into a save format enumerated value. |
| static [DetectFileFormat](./detectfileformat/)(const System::String\&) | Detects and returns the information about a format of a document stored in a disk file. |
| static [DetectFileFormat](./detectfileformat/)(const System::SharedPtr\<System::IO::Stream\>\&) | Detects and returns the information about a format of a document stored in a stream. |
| static [DetectFileFormat](./detectfileformat/)(std::basic_istream\<CharType, Traits\>\&) |  |
| static [ExtensionToSaveFormat](./extensiontosaveformat/)(const System::String\&) | Converts a file name extension into a [SaveFormat](../saveformat/) value. |
| [FileFormatUtil](./fileformatutil/)() |  |
| static [ImageTypeToExtension](./imagetypetoextension/)(Aspose::Words::Drawing::ImageType) | Converts an Aspose.Words image type enumerated value into a file extension. The returned extension is a lower-case string with a leading dot. |
| static [LoadFormatToExtension](./loadformattoextension/)(Aspose::Words::LoadFormat) | Converts a load format enumerated value into a file extension. The returned extension is a lower-case string with a leading dot. |
| static [LoadFormatToSaveFormat](./loadformattosaveformat/)(Aspose::Words::LoadFormat) | Converts a [LoadFormat](../loadformat/) value to a [SaveFormat](../saveformat/) value if possible. |
| static [SaveFormatToExtension](./saveformattoextension/)(Aspose::Words::SaveFormat) | Converts a save format enumerated value into a file extension. The returned extension is a lower-case string with a leading dot. |
| static [SaveFormatToLoadFormat](./saveformattoloadformat/)(Aspose::Words::SaveFormat) | Converts a [SaveFormat](../saveformat/) value to a [LoadFormat](../loadformat/) value if possible. |

## Examples



Shows how to detect encoding in an html file. 
```cpp
System::SharedPtr<Aspose::Words::FileFormatInfo> info = Aspose::Words::FileFormatUtil::DetectFileFormat(get_MyDir() + u"Document.html");

ASSERT_EQ(Aspose::Words::LoadFormat::Html, info->get_LoadFormat());

// The Encoding property is used only when we create a FileFormatInfo object for an html document.
ASSERT_EQ(u"Western European (Windows)", info->get_Encoding()->get_EncodingName());
ASSERT_EQ(1252, info->get_Encoding()->get_CodePage());
```

## See Also

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
