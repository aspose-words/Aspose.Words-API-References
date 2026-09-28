---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ScaleImageToShapeSize метод"
linktitle: "get_ScaleImageToShapeSize"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ScaleImageToShapeSize метод. Указывает, масштабируются ли изображения Aspose.Words до размеров ограничивающей формы при экспорте в HTML, MHTML или EPUB. Значение по умолчанию — true в C++."
type: docs
weight: 46000
url: /ru/cpp/aspose.words.saving/htmlsaveoptions/get_scaleimagetoshapesize/
---
## HtmlSaveOptions::get_ScaleImageToShapeSize method


Указывает, масштабируются ли изображения Aspose.Words до размеров ограничивающей формы при экспорте в HTML, MHTML или EPUB. Значение по умолчанию — **true**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ScaleImageToShapeSize() const
```

## Примечания


Изображение в документе Microsoft Word является фигурой. Фигура имеет размер, а изображение — свой собственный размер. Эти размеры не связаны напрямую. Например, изображение может иметь размеры 1024×786 пикселей, но фигура, отображающая это изображение, может быть 400×300 пунктов.

Чтобы отобразить изображение в браузере, его необходимо масштабировать до размера фигуры. Свойство [ScaleImageToShapeSize](./) управляет тем, где происходит масштабирование изображения: в Aspose.Words во время экспорта в HTML или в браузере при отображении документа.

Когда [ScaleImageToShapeSize](./) **true**, изображение масштабируется [Aspose.Words](../../../aspose.words/) с использованием высококачественного масштабирования во время экспорта в HTML. Когда [ScaleImageToShapeSize](./) **false**, изображение выводится с оригинальным размером, и браузеру придётся масштабировать его.

В целом, браузеры выполняют быстрое, но низкокачественное масштабирование. В результате обычно получается лучшее качество отображения в браузере и меньший размер файла, когда [ScaleImageToShapeSize](./) **true**, но лучшее качество печати и более быстрая конверсия, когда [ScaleImageToShapeSize](./) **false**.

Помимо фигур, содержащих отдельные растровые изображения, эта опция также влияет на групповые фигуры, состоящие из растровых изображений. Если [ScaleImageToShapeSize](./) имеет значение **false** и групповая фигура содержит растровые изображения, чье внутреннее разрешение выше значения, указанного в [ImageResolution](../get_imageresolution/), Aspose.Words увеличит разрешение рендеринга для этой группы. Это позволяет лучше сохранять качество сгруппированных изображений высокого разрешения при сохранении в HTML.

## См. также

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
