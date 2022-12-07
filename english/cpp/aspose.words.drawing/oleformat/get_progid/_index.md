---
title: get_ProgId
second_title: Aspose.Words for C++ API Reference
description: Gets or sets the ProgID of the OLE object.
type: docs
weight: 118
url: /cpp/aspose.words.drawing/oleformat/get_progid/
---
## OleFormat::get_ProgId method


Gets or sets the ProgID of the OLE object.

```cpp
System::String Aspose::Words::Drawing::OleFormat::get_ProgId()
```

## Remarks


The ProgID property is not always present in Microsoft Word documents and cannot be relied upon.

Cannot be **null**.

The default value is an empty string.

## Examples



Shows how to extract embedded OLE objects into files. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"OLE spreadsheet.docm");
auto shape = System::DynamicCast<Shape>(doc->GetChild(NodeType::Shape, 0, true));

// The OLE object in the first shape is a Microsoft Excel spreadsheet.
SharedPtr<OleFormat> oleFormat = shape->get_OleFormat();

ASSERT_EQ(u"Excel.Sheet.12", oleFormat->get_ProgId());

// Our object is neither auto updating nor locked from updates.
ASSERT_FALSE(oleFormat->get_AutoUpdate());
ASPOSE_ASSERT_EQ(false, oleFormat->get_IsLocked());

// If we plan on saving the OLE object to a file in the local file system,
// we can use the "SuggestedExtension" property to determine which file extension to apply to the file.
ASSERT_EQ(u".xlsx", oleFormat->get_SuggestedExtension());

// Below are two ways of saving an OLE object to a file in the local file system.
// 1 -  Save it via a stream:
{
    auto fs = MakeObject<System::IO::FileStream>(ArtifactsDir + u"OLE spreadsheet extracted via stream" + oleFormat->get_SuggestedExtension(),
                                                 System::IO::FileMode::Create);
    oleFormat->Save(fs);
}

// 2 -  Save it directly to a filename:
oleFormat->Save(ArtifactsDir + u"OLE spreadsheet saved directly" + oleFormat->get_SuggestedExtension());
```

## See Also

* Class [OleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words](../../../)
