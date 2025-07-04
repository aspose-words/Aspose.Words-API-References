---
title: Aspose::Words::DocumentBuilder::InsertOleObjectAsIcon method
linktitle: InsertOleObjectAsIcon
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::DocumentBuilder::InsertOleObjectAsIcon method. Inserts an embedded OLE object as icon from a stream into the document. Allows to specify icon file and caption. Detects OLE object type using given progID parameter in C++.'
type: docs
weight: 42000
url: /cpp/aspose.words/documentbuilder/insertoleobjectasicon/
---
## DocumentBuilder::InsertOleObjectAsIcon(const System::SharedPtr\<System::IO::Stream\>\&, const System::String\&, const System::String\&, const System::String\&) method


Inserts an embedded OLE object as icon from a stream into the document. Allows to specify icon file and caption. Detects OLE object type using given progID parameter.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObjectAsIcon(const System::SharedPtr<System::IO::Stream> &stream, const System::String &progId, const System::String &iconFile, const System::String &iconCaption)
```


| Parameter | Type | Description |
| --- | --- | --- |
| stream | const System::SharedPtr\<System::IO::Stream\>\& | Stream containing application data. |
| progId | const System::String\& | ProgId of OLE object. |
| iconFile | const System::String\& | Full path to the ICO file. If the value is **null**, Aspose.Words will use a predefined image. |
| iconCaption | const System::String\& | Icon caption. If the value is **null**, Aspose.Words will use the a predefined icon caption. |

### ReturnValue

Shape node containing Ole object and inserted at the current Builder position.

## Examples



Shows how to insert an embedded or linked OLE object as icon into the document. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// If 'iconFile' and 'iconCaption' are omitted, this overloaded method selects
// the icon according to 'progId' and uses the filename for the icon caption.
builder->InsertOleObjectAsIcon(get_MyDir() + u"Presentation.pptx", u"Package", false, get_ImageDir() + u"Logo icon.ico", u"My embedded file");

builder->InsertBreak(Aspose::Words::BreakType::LineBreak);

{
    auto stream = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Presentation.pptx", System::IO::FileMode::Open);
    // If 'iconFile' and 'iconCaption' are omitted, this overloaded method selects
    // the icon according to the file extension and uses the filename for the icon caption.
    System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertOleObjectAsIcon(stream, u"PowerPoint.Application", get_ImageDir() + u"Logo icon.ico", u"My embedded file stream");

    System::SharedPtr<Aspose::Words::Drawing::OlePackage> setOlePackage = shape->get_OleFormat()->get_OlePackage();
    setOlePackage->set_FileName(u"Presentation.pptx");
    setOlePackage->set_DisplayName(u"Presentation.pptx");
}

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertOleObjectAsIcon.docx");
```

## See Also

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOleObjectAsIcon(const System::String\&, bool, const System::String\&, const System::String\&) method


Inserts an embedded or linked OLE object as icon into the document. Allows to specify icon file and caption. Detects OLE object type using file extension.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObjectAsIcon(const System::String &fileName, bool isLinked, const System::String &iconFile, const System::String &iconCaption)
```


| Parameter | Type | Description |
| --- | --- | --- |
| fileName | const System::String\& | Full path to the file. |
| isLinked | bool | If **true** then linked OLE object is inserted otherwise embedded OLE object is inserted. |
| iconFile | const System::String\& | Full path to the ICO file. If the value is **null**, Aspose.Words will use a predefined image. |
| iconCaption | const System::String\& | Icon caption. If the value is **null**, Aspose.Words will use the file name. |

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
## DocumentBuilder::InsertOleObjectAsIcon(const System::String\&, const System::String\&, bool, const System::String\&, const System::String\&) method


Inserts an embedded or linked OLE object as icon into the document. Allows to specify icon file and caption. Detects OLE object type using given progID parameter.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObjectAsIcon(const System::String &fileName, const System::String &progId, bool isLinked, const System::String &iconFile, const System::String &iconCaption)
```


| Parameter | Type | Description |
| --- | --- | --- |
| fileName | const System::String\& | Full path to the file. |
| progId | const System::String\& | ProgId of OLE object. |
| isLinked | bool | If **true** then linked OLE object is inserted otherwise embedded OLE object is inserted. |
| iconFile | const System::String\& | Full path to the ICO file. If the value is **null**, Aspose.Words will use a predefined image. |
| iconCaption | const System::String\& | Icon caption. If the value is **null**, Aspose.Words will use the file name. |

### ReturnValue

Shape node containing Ole object and inserted at the current Builder position.

## Examples



Shows how to insert an embedded or linked OLE object as icon into the document. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// If 'iconFile' and 'iconCaption' are omitted, this overloaded method selects
// the icon according to 'progId' and uses the filename for the icon caption.
builder->InsertOleObjectAsIcon(get_MyDir() + u"Presentation.pptx", u"Package", false, get_ImageDir() + u"Logo icon.ico", u"My embedded file");

builder->InsertBreak(Aspose::Words::BreakType::LineBreak);

{
    auto stream = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Presentation.pptx", System::IO::FileMode::Open);
    // If 'iconFile' and 'iconCaption' are omitted, this overloaded method selects
    // the icon according to the file extension and uses the filename for the icon caption.
    System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertOleObjectAsIcon(stream, u"PowerPoint.Application", get_ImageDir() + u"Logo icon.ico", u"My embedded file stream");

    System::SharedPtr<Aspose::Words::Drawing::OlePackage> setOlePackage = shape->get_OleFormat()->get_OlePackage();
    setOlePackage->set_FileName(u"Presentation.pptx");
    setOlePackage->set_DisplayName(u"Presentation.pptx");
}

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertOleObjectAsIcon.docx");
```

## See Also

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOleObjectAsIcon(std::basic_istream\<CharType, Traits\>\&, System::String, System::String, System::String) method




```cpp
template<typename CharType,typename Traits> System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObjectAsIcon(std::basic_istream<CharType, Traits> &stream, System::String progId, System::String iconFile, System::String iconCaption)
```

## See Also

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
