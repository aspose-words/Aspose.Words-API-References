---
title: "Aspose::Words::Drawing::ImageData::ToStream yöntemi"
linktitle: "ToStream"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::ImageData::ToStream yöntemi. C++'ta görüntü baytlarını içeren bir akış oluşturur ve döndürür."
type: docs
weight: 38000
url: /tr/cpp/aspose.words.drawing/imagedata/tostream/
---
## ImageData::ToStream method


Görüntü baytlarını içeren bir akış oluşturur ve döndürür.

```cpp
System::SharedPtr<System::IO::Stream> Aspose::Words::Drawing::ImageData::ToStream()
```

## Açıklamalar


Eğer görüntü baytları şekil içinde depolanmışsa, bir **MemoryStream** nesnesi oluşturur ve döndürür.

Eğer görüntü bağlanmış ve bir dosyada depolanmışsa, dosyayı açar ve bir **FileStream** nesnesi döndürür.

Eğer görüntü bağlanmış ve harici bir URL'de depolanmışsa, dosyayı indirir ve bir **MemoryStream** nesnesi döndürür.

Akış nesnesini serbest bırakmak çağıranın sorumluluğu mudur?

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
