---
title: "Aspose::Words::Drawing::ShapeBase::get_IsDeleteRevision метод"
linktitle: "get_IsDeleteRevision"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::ShapeBase::get_IsDeleteRevision метод. Возвращает true, если этот объект был удалён в Microsoft Word при включённом отслеживании изменений в C++."
type: docs
weight: 26000
url: /ru/cpp/aspose.words.drawing/shapebase/get_isdeleterevision/
---
## ShapeBase::get_IsDeleteRevision method


Возвращает true, если этот объект был удалён в Microsoft Word при включённом отслеживании изменений.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_IsDeleteRevision()
```


## Примеры



Показывает, как работать с фигурами‑ревизиями.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

ASSERT_FALSE(doc->get_TrackRevisions());

// Вставьте встроенную фигуру без отслеживания изменений, что сделает эту фигуру не являющейся ревизией любого типа.
auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Cube);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::Inline);
shape->set_Width(100.0);
shape->set_Height(100.0);
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

// Начните отслеживание изменений и затем вставьте другую фигуру, которая будет ревизией.
doc->StartTrackRevisions(u"John Doe");

shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Sun);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::Inline);
shape->set_Width(100.0);
shape->set_Height(100.0);
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::Shape>> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_ToArray();

ASSERT_EQ(2, shapes->get_Length());

shapes[0]->Remove();

// Поскольку мы удалили эту фигуру, пока отслеживали изменения,
// фигура остаётся в документе и считается удалённой ревизией.
// Принятие этой ревизии удалит фигуру навсегда, а отклонение оставит её в документе.
ASSERT_EQ(Aspose::Words::Drawing::ShapeType::Cube, shapes[0]->get_ShapeType());
ASSERT_TRUE(shapes[0]->get_IsDeleteRevision());

// И мы вставили другую фигуру во время отслеживания изменений, поэтому эта фигура будет считаться вставкой‑ревизией.
// Принятие этой ревизии включит эту фигуру в документ как обычный элемент,
// а отклонение ревизии удалит эту фигуру навсегда.
ASSERT_EQ(Aspose::Words::Drawing::ShapeType::Sun, shapes[1]->get_ShapeType());
ASSERT_TRUE(shapes[1]->get_IsInsertRevision());
```

## См. также

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
