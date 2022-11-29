---
title: get_Encoding
second_title: Aspose.Words for C++ API Reference
description: Gets or sets the encoding that will be used to load an HTML, TXT, or CHM document if the encoding is not specified inside the document. Can be null. Default is null.
type: docs
weight: 53
url: /cpp/aspose.words.loading/loadoptions/get_encoding/
---
## LoadOptions::get_Encoding method


Gets or sets the encoding that will be used to load an HTML, TXT, or CHM document if the encoding is not specified inside the document. Can be null. Default is null.

```cpp
System::SharedPtr<System::Text::Encoding> Aspose::Words::Loading::LoadOptions::get_Encoding() const
```

## Remarks


This property is used only when loading HTML, TXT, or CHM documents.

If encoding is not specified inside the document and this property is **null**, then the system will try to automatically detect the encoding.

## Examples



Shows how to set the encoding with which to open a document. 
```cpp
// A FileFormatInfo object will detect this file as being encoded in something other than UTF-7.
SharedPtr<FileFormatInfo> fileFormatInfo = FileFormatUtil::DetectFileFormat(MyDir + u"Encoded in UTF-7.txt");

ASPOSE_ASSERT_NE(System::Text::Encoding::get_UTF7(), fileFormatInfo->get_Encoding());

// If we load the document with no loading configurations, Aspose.Words will detect its encoding as UTF-8.
auto doc = MakeObject<Document>(MyDir + u"Encoded in UTF-7.txt");

// The contents, parsed in UTF-8, create a valid string.
// However, knowing that the file is in UTF-7, we can see that the result is incorrect.
ASSERT_EQ(u"Hello world+ACE-", doc->ToString(SaveFormat::Text).Trim());

// In cases of ambiguous encoding such as this one, we can set a specific encoding variant
// to parse the file within a LoadOptions object.
auto loadOptions = MakeObject<LoadOptions>();
loadOptions->set_Encoding(System::Text::Encoding::get_UTF7());

// Load the document while passing the LoadOptions object, then verify the document's contents.
doc = MakeObject<Document>(MyDir + u"Encoded in UTF-7.txt", loadOptions);

ASSERT_EQ(u"Hello world!", doc->ToString(SaveFormat::Text).Trim());
```

## See Also

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words](../../../)
