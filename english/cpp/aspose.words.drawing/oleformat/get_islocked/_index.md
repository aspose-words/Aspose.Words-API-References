---
title: Aspose::Words::Drawing::OleFormat::get_IsLocked method
linktitle: get_IsLocked
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::OleFormat::get_IsLocked method. Specifies whether the link to the OLE object is locked from updates in C++.'
type: docs
weight: 6000
url: /cpp/aspose.words.drawing/oleformat/get_islocked/
---
## OleFormat::get_IsLocked method


Specifies whether the link to the OLE object is locked from updates.

```cpp
bool Aspose::Words::Drawing::OleFormat::get_IsLocked()
```

## Remarks


The default value is **false**.

## Examples



Shows how to extract embedded OLE objects into files. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"OLE spreadsheet.docm");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

// The OLE object in the first shape is a Microsoft Excel spreadsheet.
System::SharedPtr<Aspose::Words::Drawing::OleFormat> oleFormat = shape->get_OleFormat();

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
    auto fs = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"OLE spreadsheet extracted via stream" + oleFormat->get_SuggestedExtension(), System::IO::FileMode::Create);
    oleFormat->Save(fs);
}

// 2 -  Save it directly to a filename:
oleFormat->Save(get_ArtifactsDir() + u"OLE spreadsheet saved directly" + oleFormat->get_SuggestedExtension());
```

## See Also

* Class [OleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
