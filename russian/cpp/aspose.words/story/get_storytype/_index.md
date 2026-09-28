---
title: "Aspose::Words::Story::get_StoryType method"
linktitle: "get_StoryType"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Story::get_StoryType. Получает тип этой истории в C++."
type: docs
weight: 7000
url: /ru/cpp/aspose.words/story/get_storytype/
---
## Story::get_StoryType method


Возвращает тип этой истории.

```cpp
Aspose::Words::StoryType Aspose::Words::Story::get_StoryType() override
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

* Enum [StoryType](../../storytype/)
* Class [Story](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
