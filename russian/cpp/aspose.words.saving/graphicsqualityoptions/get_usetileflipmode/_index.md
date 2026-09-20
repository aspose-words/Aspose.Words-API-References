---
title: "Aspose::Words::Saving::GraphicsQualityOptions::get_UseTileFlipMode метод"
linktitle: "get_UseTileFlipMode"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::GraphicsQualityOptions::get_UseTileFlipMode метод. Возвращает или задает флаг, указывающий, используется ли WrapMode со значением TileFlipXY в C++."
type: docs
weight: 9000
url: /ru/cpp/aspose.words.saving/graphicsqualityoptions/get_usetileflipmode/
---
## GraphicsQualityOptions::get_UseTileFlipMode method


Получает или задает флаг, указывающий, является ли WrapMode значением TileFlipXY.

```cpp
bool Aspose::Words::Saving::GraphicsQualityOptions::get_UseTileFlipMode() const
```

## Примечания


Элемент **WrapMode** указывает, как текстура или градиент заполняются плиткой, когда они меньше области, которую нужно заполнить.

По умолчанию используется **Tile** (указывает на заполнение без отражения). Это приводит к неточной отрисовке масштабированного изображения (с высоким разрешением).

Это свойство позволяет переключить WrapMode на **TileFlipXY** (указывает, что плитки отражаются горизонтально при перемещении вдоль строки и вертикально при перемещении вдоль столбца).
## См. также

* Class [GraphicsQualityOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
