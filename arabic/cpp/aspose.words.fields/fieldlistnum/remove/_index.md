---
title: "Aspose::Words::Fields::FieldListNum::Remove طريقة"
linktitle: "Remove"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Fields::FieldListNum::Remove. يزيل الحقل من المستند. يُرجع عقدة مباشرة بعد الحقل. إذا كان نهاية الحقل هي الطفل الأخير لعقدة الوالد، يُرجع الفقرة الأم. إذا كان الحقل قد أُزيل بالفعل، يُرجع null في C++."
type: docs
weight: 7500
url: /ar/cpp/aspose.words.fields/fieldlistnum/remove/
---
## FieldListNum::Remove method


يزيل الحقل من المستند. يعيد عقدة مباشرةً بعد الحقل. إذا كانت نهاية الحقل هي الطفل الأخير لعقدة الوالد، يعيد الفقرة الأم. إذا كان الحقل قد أُزيل بالفعل، يعيد **null**.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::Fields::FieldListNum::Remove() override
```


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

* Class [Node](../../../aspose.words/node/)
* Class [FieldListNum](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
