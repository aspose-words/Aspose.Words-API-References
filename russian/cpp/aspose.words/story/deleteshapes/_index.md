---
title: "Метод Aspose::Words::Story::DeleteShapes"
linktitle: "DeleteShapes"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Story::DeleteShapes. Удаляет все фигуры из текста этой истории в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words/story/deleteshapes/
---
## Story::DeleteShapes method


Удаляет все фигуры из текста этой истории.

```cpp
void Aspose::Words::Story::DeleteShapes()
```


## Примеры



Показывает, как удалить все фигуры из узла.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Используйте DocumentBuilder для вставки фигуры. Это встроенная фигура,
// которая имеет родительский Paragraph, являющийся дочерним узлом Body первой секции.
builder->InsertShape(Aspose::Words::Drawing::ShapeType::Cube, 100.0, 100.0);

ASSERT_EQ(1, doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());

// Мы можем удалить все фигуры из дочерних абзацев этого Body.
ASSERT_EQ(Aspose::Words::StoryType::MainText, doc->get_FirstSection()->get_Body()->get_StoryType());
doc->get_FirstSection()->get_Body()->DeleteShapes();

ASSERT_EQ(0, doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());
```

## См. также

* Class [Story](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
