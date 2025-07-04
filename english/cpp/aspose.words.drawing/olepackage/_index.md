---
title: Aspose::Words::Drawing::OlePackage class
linktitle: OlePackage
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::OlePackage class. Allows to access OLE Package properties. To learn more, visit the  documentation article in C++.'
type: docs
weight: 9000
url: /cpp/aspose.words.drawing/olepackage/
---
## OlePackage class


Allows to access OLE Package properties. To learn more, visit the [Working with Ole Objects](https://docs.aspose.com/words/cpp/working-with-ole-objects/) documentation article.

```cpp
class OlePackage : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [get_DisplayName](./get_displayname/)() const | Gets or sets OLE Package display name. |
| [get_FileName](./get_filename/)() const | Gets or sets OLE Package file name. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_DisplayName](./set_displayname/)(System::String) | Setter for [Aspose::Words::Drawing::OlePackage::get_DisplayName](./get_displayname/). |
| [set_FileName](./set_filename/)(System::String) | Setter for [Aspose::Words::Drawing::OlePackage::get_FileName](./get_filename/). |
| static [Type](./type/)() |  |

## Examples



Shows how insert an OLE object into a document. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// OLE objects allow us to open other files in the local file system using another installed application
// in our operating system by double-clicking on the shape that contains the OLE object in the document body.
// In this case, our external file will be a ZIP archive.
System::ArrayPtr<uint8_t> zipFileBytes = System::IO::File::ReadAllBytes(get_DatabaseDir() + u"cat001.zip");

{
    auto stream = System::MakeObject<System::IO::MemoryStream>(zipFileBytes);
    System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertOleObject(stream, u"Package", true, nullptr);

    shape->get_OleFormat()->get_OlePackage()->set_FileName(u"Package file name.zip");
    shape->get_OleFormat()->get_OlePackage()->set_DisplayName(u"Package display name.zip");
}

doc->Save(get_ArtifactsDir() + u"Shape.InsertOlePackage.docx");
```

## See Also

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
