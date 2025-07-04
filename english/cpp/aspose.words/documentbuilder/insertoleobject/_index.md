---
title: Aspose::Words::DocumentBuilder::InsertOleObject method
linktitle: InsertOleObject
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::DocumentBuilder::InsertOleObject method. Inserts an embedded OLE object from a stream into the document in C++.'
type: docs
weight: 41000
url: /cpp/aspose.words/documentbuilder/insertoleobject/
---
## DocumentBuilder::InsertOleObject(const System::SharedPtr\<System::IO::Stream\>\&, const System::String\&, bool, const System::SharedPtr\<System::IO::Stream\>\&) method


Inserts an embedded OLE object from a stream into the document.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObject(const System::SharedPtr<System::IO::Stream> &stream, const System::String &progId, bool asIcon, const System::SharedPtr<System::IO::Stream> &presentation)
```


| Parameter | Type | Description |
| --- | --- | --- |
| stream | const System::SharedPtr\<System::IO::Stream\>\& | Stream containing application data. |
| progId | const System::String\& | Programmatic Identifier of OLE object. |
| asIcon | bool | Specifies either Iconic or Normal mode of OLE object being inserted. |
| presentation | const System::SharedPtr\<System::IO::Stream\>\& | Image presentation of OLE object. If value is **null** Aspose.Words will use one of the predefined images. |

### ReturnValue

Shape node containing Ole object and inserted at the current Builder position.

## Examples



Shows how to use document builder to embed OLE objects in a document. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insert a Microsoft Excel spreadsheet from the local file system
// into the document while keeping its default appearance.
{
    System::SharedPtr<System::IO::Stream> spreadsheetStream = System::IO::File::Open(get_MyDir() + u"Spreadsheet.xlsx", System::IO::FileMode::Open);
    builder->Writeln(u"Spreadsheet Ole object:");
    // If 'presentation' is omitted and 'asIcon' is set, this overloaded method selects
    // the icon according to 'progId' and uses the predefined icon caption.
    builder->InsertOleObject(spreadsheetStream, u"OleObject.xlsx", false, nullptr);
}

// Insert a Microsoft Powerpoint presentation as an OLE object.
// This time, it will have an image downloaded from the web for an icon.
{
    System::SharedPtr<System::IO::Stream> powerpointStream = System::IO::File::Open(get_MyDir() + u"Presentation.pptx", System::IO::FileMode::Open);
    System::ArrayPtr<uint8_t> imgBytes = System::IO::File::ReadAllBytes(get_ImageDir() + u"Logo.jpg");

    {
        auto imageStream = System::MakeObject<System::IO::MemoryStream>(imgBytes);
        builder->InsertParagraph();
        builder->Writeln(u"Powerpoint Ole object:");
        builder->InsertOleObject(powerpointStream, u"OleObject.pptx", true, imageStream);
    }
}

// Double-click these objects in Microsoft Word to open
// the linked files using their respective applications.
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertOleObjects.docx");
```

## See Also

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOleObject(const System::String\&, bool, bool, const System::SharedPtr\<System::IO::Stream\>\&) method


Inserts an embedded or linked OLE object from a file into the document. Detects OLE object type using file extension.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObject(const System::String &fileName, bool isLinked, bool asIcon, const System::SharedPtr<System::IO::Stream> &presentation)
```


| Parameter | Type | Description |
| --- | --- | --- |
| fileName | const System::String\& | Full path to the file. |
| isLinked | bool | If **true** then linked OLE object is inserted otherwise embedded OLE object is inserted. |
| asIcon | bool | Specifies either Iconic or Normal mode of OLE object being inserted. |
| presentation | const System::SharedPtr\<System::IO::Stream\>\& | Image presentation of OLE object. If value is **null** Aspose.Words will use one of the predefined images. |

### ReturnValue

Shape node containing Ole object and inserted at the current Builder position.

## Examples



Shows how to insert an OLE object into a document. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// OLE objects are links to files in our local file system that can be opened by other installed applications.
// Double clicking these shapes will launch the application, and then use it to open the linked object.
// There are three ways of using the InsertOleObject method to insert these shapes and configure their appearance.
// 1 -  Image taken from the local file system:
{
    auto imageStream = System::MakeObject<System::IO::FileStream>(get_ImageDir() + u"Logo.jpg", System::IO::FileMode::Open);
    // If 'presentation' is omitted and 'asIcon' is set, this overloaded method selects
    // the icon according to the file extension and uses the filename for the icon caption.
    builder->InsertOleObject(get_MyDir() + u"Spreadsheet.xlsx", false, false, imageStream);
}

// If 'presentation' is omitted and 'asIcon' is set, this overloaded method selects
// the icon according to 'progId' and uses the filename for the icon caption.
// 2 -  Icon based on the application that will open the object:
builder->InsertOleObject(get_MyDir() + u"Spreadsheet.xlsx", u"Excel.Sheet", false, true, nullptr);

// If 'iconFile' and 'iconCaption' are omitted, this overloaded method selects
// the icon according to 'progId' and uses the predefined icon caption.
// 3 -  Image icon that's 32 x 32 pixels or smaller from the local file system, with a custom caption:
builder->InsertOleObjectAsIcon(get_MyDir() + u"Presentation.pptx", false, get_ImageDir() + u"Logo icon.ico", u"Double click to view presentation!");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertOleObject.docx");
```

## See Also

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOleObject(const System::String\&, const System::String\&, bool, bool, const System::SharedPtr\<System::IO::Stream\>\&) method


Inserts an embedded or linked OLE object from a file into the document. Detects OLE object type using given progID parameter.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObject(const System::String &fileName, const System::String &progId, bool isLinked, bool asIcon, const System::SharedPtr<System::IO::Stream> &presentation)
```


| Parameter | Type | Description |
| --- | --- | --- |
| fileName | const System::String\& | Full path to the file. |
| progId | const System::String\& | ProgId of OLE object. |
| isLinked | bool | If **true** then linked OLE object is inserted otherwise embedded OLE object is inserted. |
| asIcon | bool | Specifies either Iconic or Normal mode of OLE object being inserted. |
| presentation | const System::SharedPtr\<System::IO::Stream\>\& | Image presentation of OLE object. If value is **null** Aspose.Words will use one of the predefined images. |

### ReturnValue

Shape node containing Ole object and inserted at the current Builder position.

## Examples



Shows how to insert an OLE object into a document. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// OLE objects are links to files in our local file system that can be opened by other installed applications.
// Double clicking these shapes will launch the application, and then use it to open the linked object.
// There are three ways of using the InsertOleObject method to insert these shapes and configure their appearance.
// 1 -  Image taken from the local file system:
{
    auto imageStream = System::MakeObject<System::IO::FileStream>(get_ImageDir() + u"Logo.jpg", System::IO::FileMode::Open);
    // If 'presentation' is omitted and 'asIcon' is set, this overloaded method selects
    // the icon according to the file extension and uses the filename for the icon caption.
    builder->InsertOleObject(get_MyDir() + u"Spreadsheet.xlsx", false, false, imageStream);
}

// If 'presentation' is omitted and 'asIcon' is set, this overloaded method selects
// the icon according to 'progId' and uses the filename for the icon caption.
// 2 -  Icon based on the application that will open the object:
builder->InsertOleObject(get_MyDir() + u"Spreadsheet.xlsx", u"Excel.Sheet", false, true, nullptr);

// If 'iconFile' and 'iconCaption' are omitted, this overloaded method selects
// the icon according to 'progId' and uses the predefined icon caption.
// 3 -  Image icon that's 32 x 32 pixels or smaller from the local file system, with a custom caption:
builder->InsertOleObjectAsIcon(get_MyDir() + u"Presentation.pptx", false, get_ImageDir() + u"Logo icon.ico", u"Double click to view presentation!");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertOleObject.docx");
```

## See Also

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOleObject(std::basic_istream\<CharType, Traits\>\&, System::String, bool, std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObject(std::basic_istream<CharType, Traits> &stream, System::String progId, bool asIcon, std::basic_istream<CharType, Traits> &presentation)
```

## See Also

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOleObject(System::String, bool, bool, std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObject(System::String fileName, bool isLinked, bool asIcon, std::basic_istream<CharType, Traits> &presentation)
```

## See Also

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOleObject(System::String, System::String, bool, bool, std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObject(System::String fileName, System::String progId, bool isLinked, bool asIcon, std::basic_istream<CharType, Traits> &presentation)
```

## See Also

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
