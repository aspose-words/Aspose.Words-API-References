---
title: InsertOleObjectAsIcon
second_title: Aspose.Words for C++ API Reference
description: Inserts an embedded OLE object as icon from a stream into the document. Allows to specify icon file and caption. Detects OLE object type using given progID parameter.
type: docs
weight: 534
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
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// If 'iconFile' and 'iconCaption' are omitted, this overloaded method selects
// the icon according to 'progId' and uses the filename for the icon caption.
builder->InsertOleObjectAsIcon(MyDir + u"Presentation.pptx", u"Package", false, ImageDir + u"Logo icon.ico", u"My embedded file");

builder->InsertBreak(BreakType::LineBreak);

{
    auto stream = MakeObject<System::IO::FileStream>(MyDir + u"Presentation.pptx", System::IO::FileMode::Open);
    // If 'iconFile' and 'iconCaption' are omitted, this overloaded method selects
    // the icon according to the file extension and uses the filename for the icon caption.
    SharedPtr<Shape> shape = builder->InsertOleObjectAsIcon(stream, u"PowerPoint.Application", ImageDir + u"Logo icon.ico", u"My embedded file stream");

    SharedPtr<OlePackage> setOlePackage = shape->get_OleFormat()->get_OlePackage();
    setOlePackage->set_FileName(u"Presentation.pptx");
    setOlePackage->set_DisplayName(u"Presentation.pptx");
}

doc->Save(ArtifactsDir + u"DocumentBuilder.InsertOleObjectAsIcon.docx");
```

## See Also

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
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

## See Also

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
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
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// If 'iconFile' and 'iconCaption' are omitted, this overloaded method selects
// the icon according to 'progId' and uses the filename for the icon caption.
builder->InsertOleObjectAsIcon(MyDir + u"Presentation.pptx", u"Package", false, ImageDir + u"Logo icon.ico", u"My embedded file");

builder->InsertBreak(BreakType::LineBreak);

{
    auto stream = MakeObject<System::IO::FileStream>(MyDir + u"Presentation.pptx", System::IO::FileMode::Open);
    // If 'iconFile' and 'iconCaption' are omitted, this overloaded method selects
    // the icon according to the file extension and uses the filename for the icon caption.
    SharedPtr<Shape> shape = builder->InsertOleObjectAsIcon(stream, u"PowerPoint.Application", ImageDir + u"Logo icon.ico", u"My embedded file stream");

    SharedPtr<OlePackage> setOlePackage = shape->get_OleFormat()->get_OlePackage();
    setOlePackage->set_FileName(u"Presentation.pptx");
    setOlePackage->set_DisplayName(u"Presentation.pptx");
}

doc->Save(ArtifactsDir + u"DocumentBuilder.InsertOleObjectAsIcon.docx");
```

## See Also

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
## DocumentBuilder::InsertOleObjectAsIcon(std::basic_istream\<CharType, Traits\>\&, System::String, System::String, System::String) method




```cpp
template<typename CharType,typename Traits> System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObjectAsIcon(std::basic_istream<CharType, Traits> &stream, System::String progId, System::String iconFile, System::String iconCaption)
```

## See Also

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
