---
title: "طريقة Aspose::Words::Fields::FieldCollection::Remove"
linktitle: "Remove"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Fields::FieldCollection::Remove. يزيل الحقل المحدد من هذه المجموعة ومن المستند في C++."
type: docs
weight: 8000
url: /ar/cpp/aspose.words.fields/fieldcollection/remove/
---
## FieldCollection::Remove method


يزيل الحقل المحدد من هذه المجموعة ومن المستند.

```cpp
void Aspose::Words::Fields::FieldCollection::Remove(const System::SharedPtr<Aspose::Words::Fields::Field> &field)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| حقل | const System::SharedPtr\<Aspose::Words::Fields::Field\>\& | حقل للإزالة. |

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

* Class [Field](../../field/)
* Class [FieldCollection](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
