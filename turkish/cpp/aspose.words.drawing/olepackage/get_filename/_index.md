---
title: "Aspose::Words::Drawing::OlePackage::get_FileName metodu"
linktitle: "get_FileName"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::OlePackage::get_FileName yöntemi. C++'de OLE Paket dosya adını alır veya ayarlar."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.drawing/olepackage/get_filename/
---
## OlePackage::get_FileName method


OLE Paket dosya adını alır veya ayarlar.

```cpp
System::String Aspose::Words::Drawing::OlePackage::get_FileName() const
```


## Örnekler



Bir OLE nesnesinin belgeye nasıl ekleneceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// OLE nesneleri, yerel dosya sistemindeki diğer dosyaları başka bir yüklü uygulama kullanarak açmamıza olanak tanır
// işletim sistemimizde, belge gövdesindeki OLE nesnesini içeren şekle çift tıklayarak.
// Bu durumda, dış dosyamız bir ZIP arşivi olacaktır.
System::ArrayPtr<uint8_t> zipFileBytes = System::IO::File::ReadAllBytes(get_DatabaseDir() + u"cat001.zip");

{
    auto stream = System::MakeObject<System::IO::MemoryStream>(zipFileBytes);
    System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertOleObject(stream, u"Package", true, nullptr);

    shape->get_OleFormat()->get_OlePackage()->set_FileName(u"Package file name.zip");
    shape->get_OleFormat()->get_OlePackage()->set_DisplayName(u"Package display name.zip");
}

doc->Save(get_ArtifactsDir() + u"Shape.InsertOlePackage.docx");
```

## Ayrıca Bakınız

* Class [OlePackage](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
