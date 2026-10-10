---
title: "Aspose::Words::Drawing::OlePackage sınıfı"
linktitle: "OlePackage"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::OlePackage sınıfı. OLE Paketi özelliklerine erişim sağlar. Daha fazla bilgi edinmek için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 9000
url: /tr/cpp/aspose.words.drawing/olepackage/
---
## OlePackage class


OLE Paket özelliklerine erişim sağlar. Daha fazla bilgi edinmek için [Working with Ole Objects](https://docs.aspose.com/words/cpp/working-with-ole-objects/) dokümantasyon makalesini ziyaret edin.

```cpp
class OlePackage : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_DisplayName](./get_displayname/)() const | OLE Paketi görüntüleme adını alır veya ayarlar. |
| [get_FileName](./get_filename/)() const | OLE Paket dosya adını alır veya ayarlar. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_DisplayName](./set_displayname/)(System::String) | Ayarlayıcı [Aspose::Words::Drawing::OlePackage::get_DisplayName](./get_displayname/). |
| [set_FileName](./set_filename/)(System::String) | Ayarlayıcı [Aspose::Words::Drawing::OlePackage::get_FileName](./get_filename/). |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
