---
title: "Метод Aspose::Words::Section::DeleteHeaderFooterShapes"
linktitle: "DeleteHeaderFooterShapes"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Section::DeleteHeaderFooterShapes. Удаляет все фигуры (объекты рисования) из колонтитулов этого раздела в C++."
type: docs
weight: 8000
url: /ru/cpp/aspose.words/section/deleteheaderfootershapes/
---
## Section::DeleteHeaderFooterShapes method


Удаляет все фигуры (объекты рисования) из колонтитулов этого раздела.

```cpp
void Aspose::Words::Section::DeleteHeaderFooterShapes()
```


## Примеры



Показывает, как удалить все фигуры из всех колонтитулов в разделе.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Создайте основной колонтитул с фигурой.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 100, 100);

// Создайте основной нижний колонтитул с изображением.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
builder->InsertImage(get_ImageDir() + u"Logo icon.ico");

ASSERT_EQ(1, doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::HeaderPrimary)->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());
ASSERT_EQ(1, doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary)->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());

// Удалите все фигуры из колонтитулов в первом разделе.
doc->get_FirstSection()->DeleteHeaderFooterShapes();

ASSERT_EQ(0, doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::HeaderPrimary)->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());
ASSERT_EQ(0, doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary)->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());
```

## См. также

* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
