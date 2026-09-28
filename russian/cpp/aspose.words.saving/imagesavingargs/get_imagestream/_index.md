---
title: "Aspose::Words::Saving::ImageSavingArgs::get_ImageStream метод"
linktitle: "get_ImageStream"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::ImageSavingArgs::get_ImageStream метод. Позволяет указать поток, в который будет сохранено изображение в C++."
type: docs
weight: 5000
url: /ru/cpp/aspose.words.saving/imagesavingargs/get_imagestream/
---
## ImageSavingArgs::get_ImageStream method


Позволяет указать поток, в который будет сохранено изображение.

```cpp
System::SharedPtr<System::IO::Stream> Aspose::Words::Saving::ImageSavingArgs::get_ImageStream() const
```

## Примечания


Это свойство позволяет сохранять изображения в потоки вместо файлов при работе с HTML.

Значение по умолчанию — **null**. Когда это свойство имеет значение **null**, изображение будет сохранено в файл, указанный в свойстве [ImageFileName](../get_imagefilename/).

Используя [IImageSavingCallback](../../iimagesavingcallback/) вы не можете заменить одно изображение другим. Он предназначен только для управления местоположением, где сохранять изображения.

## См. также

* Class [ImageSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
