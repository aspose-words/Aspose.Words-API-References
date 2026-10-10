---
title: "Aspose::Words::Fields::FieldCollection فئة"
linktitle: "FieldCollection"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Fields::FieldCollection class. مجموعة من كائنات Field تمثل الحقول في النطاق المحدد. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 23000
url: /ar/cpp/aspose.words.fields/fieldcollection/
---
## FieldCollection class


مجموعة من كائنات [Field](../field/) تمثل الحقول في النطاق المحدد. لمعرفة المزيد، زر مقالة الوثائق [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Fields::Field>>
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [Clear](./clear/)() | يزيل جميع الحقول في هذه المجموعة من المستند ومن المجموعة نفسها. |
| [get_Count](./get_count/)() | يعيد عدد الحقول في المجموعة. |
| [GetEnumerator](./getenumerator/)() override | يرجع كائن عدّاد. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | يعيد حقلًا عند الفهرس المحدد. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::SharedPtr\<Aspose::Words::Fields::Field\>\&) | يزيل الحقل المحدد من هذه المجموعة ومن المستند. |
| [RemoveAt](./removeat/)(int32_t) | يزيل حقلًا عند الفهرس المحدد من هذه المجموعة ومن المستند. |
| static [Type](./type/)() |  |
## ملاحظات


مثيل من هذه المجموعة يتنقل عبر الحقول التي تبدأ أو تقع ضمن النطاق المحدد.

مجموعة [FieldCollection](./) لا تملك الحقول التي تحتويها، بل هي مجرد اختيار للحقول.

مجموعة [FieldCollection](./) \"حية\"، أي أن التغييرات على أبناء كائن العقدة الذي تم إنشاؤها منه تنعكس فورًا في الحقول التي تُرجعها خصائص وطرق [FieldCollection](./).

## أمثلة



يوضح كيفية إزالة الحقول من مجموعة الحقول.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertField(u" DATE \\@ \"dddd, d MMMM yyyy\" ");
builder->InsertField(u" TIME ");
builder->InsertField(u" REVNUM ");
builder->InsertField(u" AUTHOR  \"John Doe\" ");
builder->InsertField(u" SUBJECT \"My Subject\" ");
builder->InsertField(u" QUOTE \"Hello world!\" ");
doc->UpdateFields();

System::SharedPtr<Aspose::Words::Fields::FieldCollection> fields = doc->get_Range()->get_Fields();

ASSERT_EQ(6, fields->get_Count());

// فيما يلي أربع طرق لإزالة الحقول من مجموعة الحقول.
// 1 -  احصل على حقل لإزالة نفسه:
fields->idx_get(0)->Remove();
ASSERT_EQ(5, fields->get_Count());

// 2 -  احصل على المجموعة لإزالة حقل نمرره إلى طريقة الإزالة الخاصة بها:
System::SharedPtr<Aspose::Words::Fields::Field> lastField = fields->idx_get(3);
fields->Remove(lastField);
ASSERT_EQ(4, fields->get_Count());

// 3 -  إزالة حقل من مجموعة عند فهرس:
fields->RemoveAt(2);
ASSERT_EQ(3, fields->get_Count());

// 4 -  إزالة جميع الحقول من المجموعة مرة واحدة:
fields->Clear();
ASSERT_EQ(0, fields->get_Count());
```

## انظر أيضًا

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
