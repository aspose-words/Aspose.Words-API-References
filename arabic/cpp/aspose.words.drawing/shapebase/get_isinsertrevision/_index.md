---
title: "Aspose::Words::Drawing::ShapeBase::get_IsInsertRevision method"
linktitle: "get_IsInsertRevision"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::ShapeBase::get_IsInsertRevision method. تُرجع true إذا تم إدراج هذا الكائن في Microsoft Word بينما كان تتبع التغييرات مفعلاً في C++."
type: docs
weight: 31000
url: /ar/cpp/aspose.words.drawing/shapebase/get_isinsertrevision/
---
## ShapeBase::get_IsInsertRevision method


يرجع true إذا تم إدراج هذا الكائن في Microsoft Word بينما كان تتبع التغييرات مفعلاً.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_IsInsertRevision()
```


## أمثلة



يظهر كيفية العمل مع أشكال المراجعة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

ASSERT_FALSE(doc->get_TrackRevisions());

// أدرج شكلاً مضمنًا دون تتبع المراجعات، مما سيجعل هذا الشكل ليس مراجعة من أي نوع.
auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Cube);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::Inline);
shape->set_Width(100.0);
shape->set_Height(100.0);
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

// ابدأ تتبع المراجعات ثم أدخل شكلاً آخر، والذي سيكون مراجعة.
doc->StartTrackRevisions(u"John Doe");

shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Sun);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::Inline);
shape->set_Width(100.0);
shape->set_Height(100.0);
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::Shape>> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_ToArray();

ASSERT_EQ(2, shapes->get_Length());

shapes[0]->Remove();

// نظرًا لأننا أزلنا ذلك الشكل بينما كنا نتتبع التغييرات،
// يبقى الشكل موجودًا في المستند ويُحسب كمراجعة حذف.
// قبول هذه المراجعة سيزيل الشكل نهائيًا، ورفضها سيبقيه في المستند.
ASSERT_EQ(Aspose::Words::Drawing::ShapeType::Cube, shapes[0]->get_ShapeType());
ASSERT_TRUE(shapes[0]->get_IsDeleteRevision());

// وقد أدخلنا شكلًا آخر أثناء تتبع التغييرات، لذا سيُحسب ذلك الشكل كمراجعة إدراج.
// قبول هذه المراجعة سيُدمج هذا الشكل في المستند كغير مراجعة،
// ورفض المراجعة سيزيل هذا الشكل نهائيًا.
ASSERT_EQ(Aspose::Words::Drawing::ShapeType::Sun, shapes[1]->get_ShapeType());
ASSERT_TRUE(shapes[1]->get_IsInsertRevision());
```

## انظر أيضًا

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
