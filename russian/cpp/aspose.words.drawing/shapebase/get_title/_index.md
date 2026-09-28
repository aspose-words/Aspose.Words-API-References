---
title: "Aspose::Words::Drawing::ShapeBase::get_Title метод"
linktitle: "get_Title"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::ShapeBase::get_Title метод. Получает или задает заголовок (подпись) текущего объекта фигуры в C++."
type: docs
weight: 51000
url: /ru/cpp/aspose.words.drawing/shapebase/get_title/
---
## ShapeBase::get_Title method


Получает или задаёт заголовок (подпись) текущего объекта фигуры.

```cpp
System::String Aspose::Words::Drawing::ShapeBase::get_Title()
```

## Примечания


По умолчанию — пустая строка.

Не может быть **null**, но может быть пустой строкой.

## Примеры



Показывает, как установить заголовок фигуры.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Создайте фигуру, задайте ей заголовок и затем добавьте её в документ.
auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Cube);
shape->set_Width(200);
shape->set_Height(200);
shape->set_Title(u"My cube");

builder->InsertNode(shape);

// Когда мы сохраняем документ с фигурой, у которой есть заголовок,
// Aspose.Words сохранит этот заголовок в Alt Text фигуры.
doc->Save(get_ArtifactsDir() + u"Shape.Title.docx");

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Shape.Title.docx");
shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

ASSERT_EQ(System::String::Empty, shape->get_Title());
ASSERT_EQ(u"Title: My cube", shape->get_AlternativeText());
```

## См. также

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
