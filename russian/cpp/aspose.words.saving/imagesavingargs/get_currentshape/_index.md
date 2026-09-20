---
title: "Метод Aspose::Words::Saving::ImageSavingArgs::get_CurrentShape"
linktitle: "get_CurrentShape"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Saving::ImageSavingArgs::get_CurrentShape. Возвращает объект ShapeBase, соответствующий фигуре или группе фигур, которые собираются быть сохранены в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.saving/imagesavingargs/get_currentshape/
---
## ImageSavingArgs::get_CurrentShape method


Возвращает объект [ShapeBase](../../../aspose.words.drawing/shapebase/), соответствующий фигуре или группе фигур, которые собираются быть сохранены.

```cpp
System::SharedPtr<Aspose::Words::Drawing::ShapeBase> Aspose::Words::Saving::ImageSavingArgs::get_CurrentShape() const
```

## Примечания


[IImageSavingCallback](../../iimagesavingcallback/) can be fired while saving either a shape or a group shape. That's why the property has [ShapeBase](../../../aspose.words.drawing/shapebase/) type. You can check whether it's a group shape comparing [ShapeType](../../../aspose.words.drawing/shapebase/get_shapetype/) with [Group](../../../aspose.words.drawing/shapetype/) or by casting it to one of derived classes: [Shape](../../../aspose.words.drawing/shape/) or [GroupShape](../../../aspose.words.drawing/groupshape/).

Aspose.Words использует имя файла документа и уникальный номер для генерации уникального имени файла для каждого изображения, найденного в документе. Вы можете использовать свойство [CurrentShape](./) для создания «лучшего» имени файла, анализируя свойства фигуры, такие как [Title](../../../aspose.words.drawing/imagedata/get_title/) (только для Shape), [SourceFullName](../../../aspose.words.drawing/imagedata/get_sourcefullname/) (только для Shape) и [Name](../../../aspose.words.drawing/shapebase/get_name/). Конечно, вы можете формировать имена файлов, используя любые другие свойства или критерии, но имейте в виду, что дочерние имена файлов должны быть уникальными в рамках операции экспорта.

Некоторые изображения в документе могут быть недоступны. Чтобы проверить доступность изображения, используйте свойство [IsImageAvailable](../get_isimageavailable/).
## См. также

* Class [ShapeBase](../../../aspose.words.drawing/shapebase/)
* Class [ImageSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
