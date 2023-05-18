---
title: Aspose::Words::Drawing::OleFormat::get_OlePackage method
linktitle: get_OlePackage
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::OleFormat::get_OlePackage method. Provide access to OlePackage if OLE object is an OLE Package. Returns null otherwise in C++.'
type: docs
weight: 9000
url: /cpp/aspose.words.drawing/oleformat/get_olepackage/
---
## OleFormat::get_OlePackage method


Provide access to [OlePackage](../../olepackage/) if OLE object is an OLE Package. Returns **null** otherwise.

```cpp
System::SharedPtr<Aspose::Words::Drawing::OlePackage> Aspose::Words::Drawing::OleFormat::get_OlePackage()
```


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

## See Also

* Class [OlePackage](../../olepackage/)
* Class [OleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
