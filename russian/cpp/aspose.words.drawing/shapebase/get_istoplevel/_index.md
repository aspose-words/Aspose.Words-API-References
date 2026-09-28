---
title: "Метод Aspose::Words::Drawing::ShapeBase::get_IsTopLevel"
linktitle: "get_IsTopLevel"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Drawing::ShapeBase::get_IsTopLevel. Возвращает true, если эта фигура не является дочерней для групповой фигуры в C++."
type: docs
weight: 36000
url: /ru/cpp/aspose.words.drawing/shapebase/get_istoplevel/
---
## ShapeBase::get_IsTopLevel method


Возвращает **true**, если эта фигура не является дочерней для групповой фигуры.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_IsTopLevel()
```


## Примеры



Показывает, как определить, является ли фигура частью групповой фигуры.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
shape->set_Width(200);
shape->set_Height(200);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);

// По умолчанию фигура не является частью какой-либо групповой фигуры, поэтому свойство "IsTopLevel" установлено в "true".
ASSERT_TRUE(shape->get_IsTopLevel());

auto group = System::MakeObject<Aspose::Words::Drawing::GroupShape>(doc);
group->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

// После того как мы включаем фигуру в групповую фигуру, свойство "IsTopLevel" меняется на "false".
ASSERT_FALSE(shape->get_IsTopLevel());
```

## См. также

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
