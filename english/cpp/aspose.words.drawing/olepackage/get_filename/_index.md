---
title: Aspose::Words::Drawing::OlePackage::get_FileName method
linktitle: get_FileName
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::OlePackage::get_FileName method. Gets or sets OLE Package file name in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words.drawing/olepackage/get_filename/
---
## OlePackage::get_FileName method


Gets or sets OLE Package file name.

```cpp
System::String Aspose::Words::Drawing::OlePackage::get_FileName() const
```


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

* Class [OlePackage](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
