---
title: "Aspose::Words::Drawing::ShapeBase::get_IsMoveFromRevision method"
linktitle: "get_IsMoveFromRevision"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Drawing::ShapeBase::get_IsMoveFromRevision. تُعيد true إذا تم نقل (حذف) هذا الكائن في Microsoft Word بينما كان تتبع التغييرات مفعلاً في C++."
type: docs
weight: 33000
url: /ar/cpp/aspose.words.drawing/shapebase/get_ismovefromrevision/
---
## ShapeBase::get_IsMoveFromRevision method


يرجع **true** إذا تم نقل (حذف) هذا الكائن في Microsoft Word بينما كان تتبع التغييرات مفعلاً.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_IsMoveFromRevision()
```


## أمثلة



يوضح كيفية تحديد أشكال مراجعة النقل.
```cpp
// مراجعة النقل هي عندما نقوم بنقل عنصر في جسم المستند عن طريق قصه ولصقه في Microsoft Word أثناء
// تتبع التغييرات. إذا شاركنا شكلاً مضمنًا في مثل هذه الحركة النصية، فإن ذلك الشكل سيكون أيضًا مراجعة.
// النسخ واللصق أو نقل الأشكال العائمة لا يخلق مراجعات نقل.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revision shape.docx");

// تتكون مراجعات النقل من أزواج من مراجعات \"Move from\" و\"Move to\". قمنا بالنقل في هذا المستند بشكل واحد،
// ولكن حتى نقبل أو نرفض مراجعة النقل، سيكون هناك نسختان من ذلك الشكل.
System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::Shape>> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_ToArray();

ASSERT_EQ(2, shapes->get_Length());

// هذه هي مراجعة \"Move to\"، وهي الشكل في وجهة وصوله.
// إذا قبلنا المراجعة، سيختفي شكل مراجعة \"Move to\" هذا،
// وسيظل شكل مراجعة \"Move from\".
ASSERT_FALSE(shapes[0]->get_IsMoveFromRevision());
ASSERT_TRUE(shapes[0]->get_IsMoveToRevision());

// هذه هي مراجعة \"Move from\"، وهي الشكل في موقعه الأصلي.
// إذا قبلنا المراجعة، سيختفي شكل مراجعة \"Move from\" هذا،
// وسيظل شكل مراجعة \"Move to\".
ASSERT_TRUE(shapes[1]->get_IsMoveFromRevision());
ASSERT_FALSE(shapes[1]->get_IsMoveToRevision());
```

## انظر أيضًا

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
