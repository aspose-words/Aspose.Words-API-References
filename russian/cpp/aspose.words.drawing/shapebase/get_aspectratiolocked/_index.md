---
title: "Метод Aspose::Words::Drawing::ShapeBase::get_AspectRatioLocked"
linktitle: "get_AspectRatioLocked"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Drawing::ShapeBase::get_AspectRatioLocked. Указывает, заблокировано ли соотношение сторон фигуры в C++."
type: docs
weight: 6000
url: /ru/cpp/aspose.words.drawing/shapebase/get_aspectratiolocked/
---
## ShapeBase::get_AspectRatioLocked method


Указывает, зафиксировано ли соотношение сторон фигуры.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_AspectRatioLocked()
```

## Примечания


Значение по умолчанию зависит от [ShapeType](../../shapetype/); для [Image](../../shapetype/) оно **true**, а для остальных типов фигур — **false**.

Имеет эффект только для фигур верхнего уровня.

## Примеры



Показывает, как заблокировать/разблокировать соотношение сторон фигуры.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Вставьте фигуру. Если открыть этот документ в Microsoft Word, мы можем щелкнуть левой кнопкой мыши по фигуре, чтобы увидеть
// восемь маркеров изменения размера вокруг её периметра, которые можно щёлкать и перетаскивать для изменения размера.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Установите свойство "AspectRatioLocked" в "true", чтобы сохранить соотношение сторон фигуры
// при использовании любого из четырёх диагональных маркеров изменения размера, которые изменяют как высоту, так и ширину изображения.
// Использование любых ортогональных маркеров изменения размера, меняющих высоту или ширину, всё равно изменит соотношение сторон.
// Установите свойство "AspectRatioLocked" в "false", чтобы позволить нам
// свободно менять соотношение сторон изображения всеми маркерами изменения размера.
shape->set_AspectRatioLocked(lockAspectRatio);

doc->Save(get_ArtifactsDir() + u"Shape.AspectRatio.docx");
```

## См. также

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
