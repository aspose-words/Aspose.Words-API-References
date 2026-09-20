---
title: "Aspose::Words::Drawing::SoftEdgeFormat class"
linktitle: "SoftEdgeFormat"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::SoftEdgeFormat class. Представляет форматирование мягких краёв для объекта в C++."
type: docs
weight: 13500
url: /ru/cpp/aspose.words.drawing/softedgeformat/
---
## SoftEdgeFormat class


Представляет форматирование мягкой границы для объекта.

```cpp
class SoftEdgeFormat : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_Radius](./get_radius/)() | Получает или задаёт значение типа double, которое представляет длину радиуса эффекта мягкого края в пунктах (pt). Значение по умолчанию — 0,0. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)() | Удаляет [SoftEdgeFormat](./) из родительского объекта. |
| [set_Radius](./set_radius/)(double) | Сеттер для [Aspose::Words::Drawing::SoftEdgeFormat::get_Radius](./get_radius/). |
| static [Type](./type/)() |  |
## Примечания


Используйте свойство [SoftEdge](../shapebase/get_softedge/), чтобы получить доступ к свойствам мягкого края объекта. Вы не создаёте экземпляры класса [SoftEdgeFormat](./) напрямую.

## Примеры



Показывает, как работать с форматированием мягкого края.
```cpp
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 200, 200);

// Примените мягкий край к фигуре.
shape->get_SoftEdge()->set_Radius(30);

builder->get_Document()->Save(get_ArtifactsDir() + u"Shape.SoftEdge.docx");

// Загрузите документ с прямоугольной фигурой с мягким краем.
auto doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Shape.SoftEdge.docx");
shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::SoftEdgeFormat> softEdgeFormat = shape->get_SoftEdge();

// Проверьте радиус мягкого края.
ASPOSE_ASSERT_EQ(30, softEdgeFormat->get_Radius());

// Удалить мягкую кромку из фигуры.
softEdgeFormat->Remove();

// Проверьте радиус удалённой мягкой кромки.
ASPOSE_ASSERT_EQ(0, softEdgeFormat->get_Radius());
```

## См. также

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
