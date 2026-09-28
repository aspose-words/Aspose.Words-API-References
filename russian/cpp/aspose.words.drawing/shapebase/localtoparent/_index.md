---
title: "Aspose::Words::Drawing::ShapeBase::LocalToParent метод"
linktitle: "LocalToParent"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::ShapeBase::LocalToParent метод. Преобразует значение из локального пространства координат в пространство координат родительской фигуры в C++."
type: docs
weight: 61000
url: /ru/cpp/aspose.words.drawing/shapebase/localtoparent/
---
## ShapeBase::LocalToParent method


Преобразует значение из локального пространства координат в пространство координат родительской фигуры.

```cpp
System::Drawing::PointF Aspose::Words::Drawing::ShapeBase::LocalToParent(System::Drawing::PointF value)
```


## Примеры



Показывает, как преобразовать положение координат x и y на координатной плоскости фигуры в положение на координатной плоскости родительской фигуры.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Вставьте групповую фигуру и разместите её на 100 пунктов ниже и правее
// от исходной точки координат x и Y документа.
auto group = System::MakeObject<Aspose::Words::Drawing::GroupShape>(doc);
group->set_Bounds(System::Drawing::RectangleF(100.0f, 100.0f, 500.0f, 500.0f));

// Используйте метод "LocalToParent", чтобы определить, что (0, 0) во внутренних координатах x и y группы
// соответствует (100, 100) в координатной системе её родительской фигуры. Родителем групповой фигуры является сам документ.
ASPOSE_ASSERT_EQ(System::Drawing::PointF(100.0f, 100.0f), group->LocalToParent(System::Drawing::PointF(0.0f, 0.0f)));

// По умолчанию внутренняя координатная плоскость фигуры имеет верхний левый угол в (0, 0),
// а нижний правый угол в (1000, 1000). Из‑за своего размера наша групповая фигура покрывает область 500pt × 500pt
// в плоскости документа. Это означает, что перемещение на 1pt в координатной плоскости документа будет преобразовано
// в перемещение на 2pt в координатной плоскости групповой фигуры.
ASPOSE_ASSERT_EQ(System::Drawing::PointF(150.0f, 150.0f), group->LocalToParent(System::Drawing::PointF(100.0f, 100.0f)));
ASPOSE_ASSERT_EQ(System::Drawing::PointF(200.0f, 200.0f), group->LocalToParent(System::Drawing::PointF(200.0f, 200.0f)));
ASPOSE_ASSERT_EQ(System::Drawing::PointF(250.0f, 250.0f), group->LocalToParent(System::Drawing::PointF(300.0f, 300.0f)));

// Переместите начало координат осей x и y группы фигур из верхнего левого угла в центр.
// Это сместит внутренние координаты группы относительно координат документа ещё дальше.
group->set_CoordOrigin(System::Drawing::Point(-250, -250));

ASPOSE_ASSERT_EQ(System::Drawing::PointF(375.0f, 375.0f), group->LocalToParent(System::Drawing::PointF(300.0f, 300.0f)));

// Изменение масштаба координатной плоскости также повлияет на относительные положения.
group->set_CoordSize(System::Drawing::Size(500, 500));

ASPOSE_ASSERT_EQ(System::Drawing::PointF(650.0f, 650.0f), group->LocalToParent(System::Drawing::PointF(300.0f, 300.0f)));

// Если мы хотим добавить фигуру в эту группу, определяя её расположение на основе положения в документе,
// нам потребуется сначала подтвердить положение в группе фигур, которое будет соответствовать положению в документе.
ASPOSE_ASSERT_EQ(System::Drawing::PointF(700.0f, 700.0f), group->LocalToParent(System::Drawing::PointF(350.0f, 350.0f)));

auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
shape->set_Width(100);
shape->set_Height(100);
shape->set_Left(700);
shape->set_Top(700);

group->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::GroupShape>>(group);

doc->Save(get_ArtifactsDir() + u"Shape.LocalToParent.docx");
```

## См. также

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
