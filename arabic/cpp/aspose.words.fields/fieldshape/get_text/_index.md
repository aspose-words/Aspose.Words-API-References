---
title: "Aspose::Words::Fields::FieldShape::get_Text طريقة"
linktitle: "get_Text"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Fields::FieldShape::get_Text طريقة. يسترجع أو يعيّن النص في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.fields/fieldshape/get_text/
---
## FieldShape::get_Text method


يحصل أو يضبط النص المراد استرجاعه.

```cpp
System::String Aspose::Words::Fields::FieldShape::get_Text()
```


## أمثلة



يُظهر كيفية إنشاء قوائم متوافقة مع اللغات من اليمين إلى اليسار باستخدام حقول BIDIOUTLINE.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// حقل BIDIOUTLINE يرقم الفقرات مثل حقول AUTONUM/LISTNUM،
// ولكنه يظهر فقط عندما يتم تمكين لغة تحرير من اليمين إلى اليسار، مثل العبرية أو العربية.
// الحقل التالي سيعرض ".1"، المكافئ RTL لرقم القائمة "1.".
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldBidiOutline>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldBidiOutline, true));
builder->Writeln(u"שלום");

ASSERT_EQ(u" BIDIOUTLINE ", field->GetFieldCode());

// أضف حقلين إضافيين من نوع BIDIOUTLINE، سيعرضان ".2" و ".3".
builder->InsertField(Aspose::Words::Fields::FieldType::FieldBidiOutline, true);
builder->Writeln(u"שלום");
builder->InsertField(Aspose::Words::Fields::FieldType::FieldBidiOutline, true);
builder->Writeln(u"שלום");

// اضبط محاذاة النص الأفقية لكل فقرة في المستند إلى RTL.
for (auto&& para : System::IterateOver<Aspose::Words::Paragraph>(doc->GetChildNodes(Aspose::Words::NodeType::Paragraph, true)))
{
    para->get_ParagraphFormat()->set_Bidi(true);
}

// إذا مكنّا لغة تحرير من اليمين إلى اليسار في Microsoft Word، ستعرض حقولنا أرقامًا.
// وإلا، ستعرض "###".
doc->Save(get_ArtifactsDir() + u"Field.BIDIOUTLINE.docx");
```


يُظهر كيف يتم التعامل مع بعض حقول Microsoft Word القديمة مثل SHAPE و EMBED أثناء التحميل.
```cpp
// افتح مستندًا تم إنشاؤه في Microsoft Word 2003.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Legacy fields.doc");

// إذا فتحنا مستند Word وضغطنا Alt+F9، سنرى حقل SHAPE وحقل EMBED.
// حقل SHAPE هو المرفق/اللوحة لكائن AutoShape مع تمكين نمط الالتفاف "In line with text".
// حقل EMBED له نفس الوظيفة، لكنه لكائن مضمّن،
// مثل جدول بيانات من مستند Excel خارجي.
// مع ذلك، هذه الحقول لن تظهر في مجموعة الحقول الخاصة بالمستند.
ASSERT_EQ(0, doc->get_Range()->get_Fields()->get_Count());

// هذه الحقول مدعومة فقط في الإصدارات القديمة من Microsoft Word.
// عملية تحميل المستند ستحول هذه الحقول إلى كائنات Shape،
// والتي يمكننا الوصول إليها في مجموعة العقد الخاصة بالمستند.
System::SharedPtr<Aspose::Words::NodeCollection> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true);
ASSERT_EQ(3, shapes->get_Count());

// العقدة الأولى من نوع Shape تتطابق مع حقل SHAPE في المستند المدخل،
// وهي اللوحة المضمنة لكائن AutoShape.
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(shapes->idx_get(0));
ASSERT_EQ(Aspose::Words::Drawing::ShapeType::Image, shape->get_ShapeType());

// العقدة الثانية من نوع Shape هي AutoShape نفسها.
shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(shapes->idx_get(1));
ASSERT_EQ(Aspose::Words::Drawing::ShapeType::Can, shape->get_ShapeType());

// العقدة الثالثة من نوع Shape هي ما كان حقل EMBED الذي يحتوي على جدول البيانات الخارجي.
shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(shapes->idx_get(2));
ASSERT_EQ(Aspose::Words::Drawing::ShapeType::OleObject, shape->get_ShapeType());
```

## انظر أيضًا

* Class [FieldShape](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
