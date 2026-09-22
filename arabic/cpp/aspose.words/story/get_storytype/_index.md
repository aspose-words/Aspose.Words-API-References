---
title: "طريقة Aspose::Words::Story::get_StoryType"
linktitle: "get_StoryType"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Story::get_StoryType. يسترجع نوع هذه القصة في C++."
type: docs
weight: 7000
url: /ar/cpp/aspose.words/story/get_storytype/
---
## Story::get_StoryType method


يحصل على نوع هذه القصة.

```cpp
Aspose::Words::StoryType Aspose::Words::Story::get_StoryType() override
```


## أمثلة



يُظهر كيفية إزالة جميع الأشكال من عقدة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// استخدم DocumentBuilder لإدراج شكل. هذا شكل مضمن،
// الذي له فقرة أصل، وهي عقدة فرعية لجسم القسم الأول.
builder->InsertShape(Aspose::Words::Drawing::ShapeType::Cube, 100.0, 100.0);

ASSERT_EQ(1, doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());

// يمكننا حذف جميع الأشكال من الفقرات الفرعية لهذا الجسم.
ASSERT_EQ(Aspose::Words::StoryType::MainText, doc->get_FirstSection()->get_Body()->get_StoryType());
doc->get_FirstSection()->get_Body()->DeleteShapes();

ASSERT_EQ(0, doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());
```

## انظر أيضًا

* Enum [StoryType](../../storytype/)
* Class [Story](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
