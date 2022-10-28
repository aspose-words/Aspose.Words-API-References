---
title: OlePackage
second_title: Aspose.Words for C++ API Reference
description: Allows to access OLE Package properties.
type: docs
weight: 105
url: /cpp/aspose.words.drawing/olepackage/
---
## OlePackage class


Allows to access OLE Package properties.

```cpp
class OlePackage : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [get_DisplayName](./get_displayname/)() const | Gets or sets OLE Package display name. |
| [get_FileName](./get_filename/)() const | Gets or sets OLE Package file name. |
| [set_DisplayName](./set_displayname/)(System::String) | Setter for [Aspose::Words::Drawing::OlePackage::get_DisplayName](./get_displayname/). |
| [set_FileName](./set_filename/)(System::String) | Setter for [Aspose::Words::Drawing::OlePackage::get_FileName](./get_filename/). |

## Examples




Shows how insert an OLE object into a document. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// OLE objects allow us to open other files in the local file system using another installed application
// in our operating system by double-clicking on the shape that contains the OLE object in the document body.
// In this case, our external file will be a ZIP archive.
ArrayPtr<uint8_t> zipFileBytes = System::IO::File::ReadAllBytes(DatabaseDir + u"cat001.zip");

{
    auto stream = MakeObject<System::IO::MemoryStream>(zipFileBytes);
    SharedPtr<Shape> shape = builder->InsertOleObject(stream, u"Package", true, nullptr);

    shape->get_OleFormat()->get_OlePackage()->set_FileName(u"Package file name.zip");
    shape->get_OleFormat()->get_OlePackage()->set_DisplayName(u"Package display name.zip");
}

doc->Save(ArtifactsDir + u"Shape.InsertOlePackage.docx");
```

