---
title: "Aspose::Words::Drawing::ImageData::ToByteArray method"
linktitle: "ToByteArray"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::ImageData::ToByteArray method. Возвращает байты изображения для любого изображения независимо от того, хранится ли изображение или связано в C++."
type: docs
weight: 36000
url: /ru/cpp/aspose.words.drawing/imagedata/tobytearray/
---
## ImageData::ToByteArray method


Возвращает байты изображения для любого изображения независимо от того, хранится ли изображение или связано.

```cpp
System::ArrayPtr<uint8_t> Aspose::Words::Drawing::ImageData::ToByteArray()
```

## Примечания


Если изображение связано, оно загружается каждый раз при вызове.

## Примеры



Показывает, как создать файл изображения из необработанных данных изображения фигуры.
```cpp
auto imgSourceDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");

auto imgShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(imgSourceDoc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

ASSERT_TRUE(imgShape->get_HasImage());

// ToByteArray() возвращает массив, хранящийся в свойстве ImageBytes.
ASPOSE_ASSERT_EQ(imgShape->get_ImageData()->get_ImageBytes(), imgShape->get_ImageData()->ToByteArray());

// Сохраните данные изображения формы в файл изображения в локальной файловой системе.
{
    System::SharedPtr<System::IO::Stream> imgStream = imgShape->get_ImageData()->ToStream();
    {
        auto outStream = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"Drawing.GetDataFromImage.png", System::IO::FileMode::Create, System::IO::FileAccess::ReadWrite);
        imgStream->CopyTo(outStream);
    }
}
```

## См. также

* Class [ImageData](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
