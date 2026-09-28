---
title: "Aspose::Words::Drawing::ShapeBase::get_BoundsWithEffects метод"
linktitle: "get_BoundsWithEffects"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::ShapeBase::get_BoundsWithEffects метод. Получает окончательный размер, который имеет этот объект формы после применения эффектов рисования. Значение измеряется в пунктах в C++."
type: docs
weight: 11000
url: /ru/cpp/aspose.words.drawing/shapebase/get_boundswitheffects/
---
## ShapeBase::get_BoundsWithEffects method


Получает окончательный размер этого объекта фигуры после применения эффектов рисования. Значение измеряется в пунктах.

```cpp
System::Drawing::RectangleF Aspose::Words::Drawing::ShapeBase::get_BoundsWithEffects()
```


## Примеры



Показывает, как проверить, как границы фигуры изменяются под воздействием эффектов.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shape shadow effect.docx");

System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::Shape>> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_ToArray();

ASSERT_EQ(2, shapes->get_Length());

// Две фигуры идентичны по размерам и типу формы.
ASPOSE_ASSERT_EQ(shapes[0]->get_Width(), shapes[1]->get_Width());
ASPOSE_ASSERT_EQ(shapes[0]->get_Height(), shapes[1]->get_Height());
ASSERT_EQ(shapes[0]->get_ShapeType(), shapes[1]->get_ShapeType());

// У первой фигуры нет эффектов, а у второй есть тень и толстый контур.
// Эти эффекты делают размер силуэта второй фигуры больше, чем у первой.
// Хотя размер прямоугольника отображается, когда мы щёлкаем по этим фигурам в Microsoft Word,
// видимые внешние границы второй фигуры изменяются под воздействием тени и контура и поэтому становятся больше.
// Мы можем использовать метод \"AdjustWithEffects\", чтобы увидеть истинный размер фигуры.
ASPOSE_ASSERT_EQ(0.0, shapes[0]->get_StrokeWeight());
ASPOSE_ASSERT_EQ(20.0, shapes[1]->get_StrokeWeight());
ASSERT_FALSE(shapes[0]->get_ShadowEnabled());
ASSERT_TRUE(shapes[1]->get_ShadowEnabled());

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = shapes[0];

// Создайте объект RectangleF, представляющий прямоугольник,
// который мы потенциально можем использовать в качестве координат и границ для фигуры.
System::Drawing::RectangleF rectangleF(200.0f, 200.0f, 1000.0f, 1000.0f);

// Выполните этот метод, чтобы получить размер прямоугольника, скорректированный с учётом всех наших эффектов фигуры.
System::Drawing::RectangleF rectangleFOut = shape->AdjustWithEffects(rectangleF);

// Поскольку у фигуры нет эффектов, изменяющих границу, её размеры границ не изменяются.
ASPOSE_ASSERT_EQ(200, rectangleFOut.get_X());
ASPOSE_ASSERT_EQ(200, rectangleFOut.get_Y());
ASPOSE_ASSERT_EQ(1000, rectangleFOut.get_Width());
ASPOSE_ASSERT_EQ(1000, rectangleFOut.get_Height());

// Проверьте окончательный охват первой фигуры в пунктах.
ASPOSE_ASSERT_EQ(0, shape->get_BoundsWithEffects().get_X());
ASPOSE_ASSERT_EQ(0, shape->get_BoundsWithEffects().get_Y());
ASPOSE_ASSERT_EQ(147, shape->get_BoundsWithEffects().get_Width());
ASPOSE_ASSERT_EQ(147, shape->get_BoundsWithEffects().get_Height());

shape = shapes[1];
rectangleF = System::Drawing::RectangleF(200.0f, 200.0f, 1000.0f, 1000.0f);
rectangleFOut = shape->AdjustWithEffects(rectangleF);

// Эффекты фигуры слегка сместили видимый верхний левый угол фигуры.
ASPOSE_ASSERT_EQ(171.5, rectangleFOut.get_X());
ASPOSE_ASSERT_EQ(167, rectangleFOut.get_Y());

// Эффекты также повлияли на видимые размеры фигуры.
ASPOSE_ASSERT_EQ(1045, rectangleFOut.get_Width());
ASPOSE_ASSERT_EQ(1133.5, rectangleFOut.get_Height());

// Эффекты также повлияли на видимые границы фигуры.
ASPOSE_ASSERT_EQ(-28.5, shape->get_BoundsWithEffects().get_X());
ASPOSE_ASSERT_EQ(-33, shape->get_BoundsWithEffects().get_Y());
ASPOSE_ASSERT_EQ(192, shape->get_BoundsWithEffects().get_Width());
ASPOSE_ASSERT_EQ(280.5, shape->get_BoundsWithEffects().get_Height());
```

## См. также

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
