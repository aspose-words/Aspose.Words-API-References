---
title: "Метод Aspose::Words::Drawing::ShapeBase::get_ZOrder"
linktitle: "get_ZOrder"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Drawing::ShapeBase::get_ZOrder. Определяет порядок отображения перекрывающихся фигур в C++."
type: docs
weight: 57000
url: /ru/cpp/aspose.words.drawing/shapebase/get_zorder/
---
## ShapeBase::get_ZOrder method


Определяет порядок отображения перекрывающихся фигур.

```cpp
int32_t Aspose::Words::Drawing::ShapeBase::get_ZOrder()
```

## Примечания


Имеет эффект только для фигур верхнего уровня.

Значение по умолчанию равно 0.

Число представляет приоритет наложения. Фигура с более высоким числом будет отображаться так, как будто она перекрывает (находится \"спереди\" ) фигуру с более низким числом.

Порядок перекрывающихся фигур независим для фигур в колонтитуле и в основном тексте документа.

Порядок отображения дочерних фигур в групповой фигуре определяется их порядком внутри групповой фигуры.

## Примеры



Показывает, как управлять порядком фигур.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Вставьте три прямоугольника разного цвета, которые частично перекрывают друг друга.
// Когда мы вставляем фигуру, перекрывающую другую фигуру, Aspose.Words размещает новую фигуру поверх старой.
// Светло-зелёный прямоугольник перекроет светло-голубой прямоугольник и частично его скроет,
// а светло-голубой прямоугольник скроет оранжевый прямоугольник.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 100, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 100, 200, 200, Aspose::Words::Drawing::WrapType::None);
shape->set_FillColor(System::Drawing::Color::get_Orange());

shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 150, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 150, 200, 200, Aspose::Words::Drawing::WrapType::None);
shape->set_FillColor(System::Drawing::Color::get_LightBlue());

shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 200, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 200, 200, 200, Aspose::Words::Drawing::WrapType::None);
shape->set_FillColor(System::Drawing::Color::get_LightGreen());

System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::Shape>> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_ToArray();

// Свойство \"ZOrder\" фигуры определяет её приоритет наложения среди других перекрывающихся фигур.
// Если у двух перекрывающихся фигур разные значения \"ZOrder\",
// Microsoft Word разместит фигуру с более высоким значением над фигурой с более низким значением.
// Установите значения \"ZOrder\" наших фигур, чтобы разместить первый оранжевый прямоугольник над вторым светло-голубым
// и второй светло-голубой прямоугольник над третьим светло-зелёным прямоугольником.
// Это изменит их исходный порядок наложения.
shapes[0]->set_ZOrder(3);
shapes[1]->set_ZOrder(2);
shapes[2]->set_ZOrder(1);

doc->Save(get_ArtifactsDir() + u"Shape.ZOrder.docx");
```

## См. также

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
