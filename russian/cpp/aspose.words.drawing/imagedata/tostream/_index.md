---
title: "Aspose::Words::Drawing::ImageData::ToStream метод"
linktitle: "ToStream"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::ImageData::ToStream метод. Создаёт и возвращает поток, содержащий байты изображения в C++."
type: docs
weight: 38000
url: /ru/cpp/aspose.words.drawing/imagedata/tostream/
---
## ImageData::ToStream method


Создаёт и возвращает поток, содержащий байты изображения.

```cpp
System::SharedPtr<System::IO::Stream> Aspose::Words::Drawing::ImageData::ToStream()
```

## Примечания


Если байты изображения хранятся в фигуре, создаёт и возвращает объект **MemoryStream**.

Если изображение связано и хранится в файле, открывает файл и возвращает объект **FileStream**.

Если изображение связано и хранится по внешнему URL, загружает файл и возвращает объект **MemoryStream**.

Является ли обязанностью вызывающего освобождать объект потока.

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
