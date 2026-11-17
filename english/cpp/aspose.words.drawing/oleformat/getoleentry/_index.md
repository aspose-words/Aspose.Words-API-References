---
title: Aspose::Words::Drawing::OleFormat::GetOleEntry method
linktitle: GetOleEntry
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::OleFormat::GetOleEntry method. Gets OLE object data entry in C++.'
type: docs
weight: 15000
url: /cpp/aspose.words.drawing/oleformat/getoleentry/
---
## OleFormat::GetOleEntry method


Gets OLE object data entry.

```cpp
System::SharedPtr<System::IO::MemoryStream> Aspose::Words::Drawing::OleFormat::GetOleEntry(const System::String & oleEntryName)
```


| Parameter | Type | Description |
| --- | --- | --- |
| oleEntryName | const System::String \& | Case-sensitive name of the OLE data stream. |

### ReturnValue

An OLE data stream or **null**.
## Examples


Shows how to insert linked and unlinked OLE objects.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Embed a Microsoft Visio drawing into the document as an OLE object.
builder->InsertOleObject(get_ImageDir() + u"Microsoft Visio drawing.vsd", u"Package", false, false, nullptr);

// Insert a link to the file in the local file system and display it as an icon.
builder->InsertOleObject(get_ImageDir() + u"Microsoft Visio drawing.vsd", u"Package", true, true, nullptr);

// Inserting OLE objects creates shapes that store these objects.
System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::Shape>> shapes = doc->GetChildNodes(NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape>>()->LINQ_ToArray();

ASSERT_EQ(shapes->get_Length(), 2);
ASSERT_EQ(shapes->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Drawing::Shape>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Drawing::Shape> s)>>([](System::SharedPtr<Aspose::Words::Drawing::Shape> s) -> bool
{
    return s->get_ShapeType() == ShapeType::OleObject;
}))), 2);

// If a shape contains an OLE object, it will have a valid "OleFormat" property,
// which we can use to verify some aspects of the shape.
System::SharedPtr<Aspose::Words::Drawing::OleFormat> oleFormat = shapes[0]->get_OleFormat();

ASPOSE_ASSERT_EQ(oleFormat->get_IsLink(), false);
ASPOSE_ASSERT_EQ(oleFormat->get_OleIcon(), false);

oleFormat = shapes[1]->get_OleFormat();

ASPOSE_ASSERT_EQ(oleFormat->get_IsLink(), true);
ASPOSE_ASSERT_EQ(oleFormat->get_OleIcon(), true);

ASSERT_TRUE(oleFormat->get_SourceFullName().EndsWith(System::String(u"Images") + System::IO::Path::DirectorySeparatorChar + u"Microsoft Visio drawing.vsd"));
ASSERT_EQ(oleFormat->get_SourceItem(), u"");

ASSERT_EQ(oleFormat->get_IconCaption(), u"Microsoft Visio drawing.vsd");

doc->Save(get_ArtifactsDir() + u"Shape.OleLinks.docx");

// If the object contains OLE data, we can access it using a stream.
{
    System::SharedPtr<System::IO::MemoryStream> stream = oleFormat->GetOleEntry(u"\x0001" u"CompObj");
    System::ArrayPtr<uint8_t> oleEntryBytes = stream->ToArray();
    ASSERT_EQ(oleEntryBytes->get_Length(), 76);
}
```
## See Also

* Class [OleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
