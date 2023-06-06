---
title: Aspose::Words::Drawing::OleFormat::Save method
linktitle: Save
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::OleFormat::Save method. Saves the data of the embedded object into the specified stream in C++.'
type: docs
weight: 19000
url: /cpp/aspose.words.drawing/oleformat/save/
---
## OleFormat::Save(const System::SharedPtr\<System::IO::Stream\>\&) method


Saves the data of the embedded object into the specified stream.

```cpp
void Aspose::Words::Drawing::OleFormat::Save(const System::SharedPtr<System::IO::Stream> &stream)
```


| Parameter | Type | Description |
| --- | --- | --- |
| stream | const System::SharedPtr\<System::IO::Stream\>\& | Where to save the object data. |
## Remarks


It is the responsibility of the caller to dispose the stream.

## Examples



Shows how to extract embedded OLE objects into files. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"OLE spreadsheet.docm");
auto shape = System::ExplicitCast<Shape>(doc->GetChild(NodeType::Shape, 0, true));

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
* Library [Aspose.Words for C++](../../../)
## OleFormat::Save(const System::String\&) method


Saves the data of the embedded object into a file with the specified name.

```cpp
void Aspose::Words::Drawing::OleFormat::Save(const System::String &fileName)
```


| Parameter | Type | Description |
| --- | --- | --- |
| fileName | const System::String\& | Name of the file to save the OLE object data. |

## Examples



Shows how to extract embedded OLE objects into files. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"OLE spreadsheet.docm");
auto shape = System::ExplicitCast<Shape>(doc->GetChild(NodeType::Shape, 0, true));

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
* Library [Aspose.Words for C++](../../../)
## OleFormat::Save(std::basic_ostream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> void Aspose::Words::Drawing::OleFormat::Save(std::basic_ostream<CharType, Traits> &stream)
```

## See Also

* Class [OleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
