---
title: "Aspose::Words::Drawing::ImageData::get_ImageBytes metodu"
linktitle: "get_ImageBytes"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::ImageData::get_ImageBytes metodu. Şekilde depolanan görüntünün ham baytlarını alır veya ayarlar C++'ta."
type: docs
weight: 13000
url: /tr/cpp/aspose.words.drawing/imagedata/get_imagebytes/
---
## ImageData::get_ImageBytes method


Şekilde depolanan görüntünün ham baytlarını alır veya ayarlar.

```cpp
System::ArrayPtr<uint8_t> Aspose::Words::Drawing::ImageData::get_ImageBytes()
```

## Açıklamalar


Değeri **null** veya boş bir diziye ayarlamak, görüntüyü şekilden kaldıracaktır.

Görüntü belgede depolanmamışsa **null** döndürür (ör. bu durumda görüntü muhtemelen bağlanmıştır).

## Örnekler



Bir şeklin ham görüntü verilerinden bir görüntü dosyası oluşturmayı gösterir.
```cpp
auto imgSourceDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");

auto imgShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(imgSourceDoc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

ASSERT_TRUE(imgShape->get_HasImage());

// ToByteArray() yöntemi, ImageBytes özelliğinde depolanan diziyi döndürür.
ASPOSE_ASSERT_EQ(imgShape->get_ImageData()->get_ImageBytes(), imgShape->get_ImageData()->ToByteArray());

// Şeklin görüntü verisini yerel dosya sisteminde bir görüntü dosyasına kaydedin.
{
    System::SharedPtr<System::IO::Stream> imgStream = imgShape->get_ImageData()->ToStream();
    {
        auto outStream = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"Drawing.GetDataFromImage.png", System::IO::FileMode::Create, System::IO::FileAccess::ReadWrite);
        imgStream->CopyTo(outStream);
    }
}
```

## Ayrıca Bakınız

* Class [ImageData](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
