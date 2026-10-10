---
title: "طريقة Aspose::Words::Story::DeleteShapes"
linktitle: "DeleteShapes"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Story::DeleteShapes. يحذف جميع الأشكال من نص هذه القصة في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words/story/deleteshapes/
---
## Story::DeleteShapes method


يحذف جميع الأشكال من نص هذه القصة.

```cpp
void Aspose::Words::Story::DeleteShapes()
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

* Class [Story](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
