---
title: "Aspose::Words::Bibliography::PersonCollection::RemoveAt طريقة"
linktitle: "RemoveAt"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Bibliography::PersonCollection::RemoveAt طريقة. يزيل الشخص عند الفهرس المحدد في C++."
type: docs
weight: 12000
url: /ar/cpp/aspose.words.bibliography/personcollection/removeat/
---
## PersonCollection::RemoveAt method


يزيل الشخص في الفهرس المحدد.

```cpp
void Aspose::Words::Bibliography::PersonCollection::RemoveAt(int32_t index)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| index | int32_t | الفهرس الصفري للشخص المراد إزالته. |

## أمثلة



يعرض كيفية العمل مع مجموعة الأشخاص.
```cpp
// إنشاء مجموعة أشخاص جديدة.
auto persons = System::MakeObject<Aspose::Words::Bibliography::PersonCollection>();
auto person = System::MakeObject<Aspose::Words::Bibliography::Person>(u"Roxanne", u"Brielle", u"Tejeda_updated");
// إضافة شخص جديد إلى المجموعة.
persons->Add(person);
ASSERT_EQ(1, persons->get_Count());
// إزالة شخص من المجموعة إذا كان موجودًا.
if (persons->Contains(person))
{
    persons->Remove(person);
}
ASSERT_EQ(0, persons->get_Count());

// إنشاء مجموعة أشخاص مع شخصين.
persons = System::MakeObject<Aspose::Words::Bibliography::PersonCollection>(System::MakeArray<System::SharedPtr<Aspose::Words::Bibliography::Person>>({System::MakeObject<Aspose::Words::Bibliography::Person>(u"Roxanne_1", u"Brielle_1", u"Tejeda_1"), System::MakeObject<Aspose::Words::Bibliography::Person>(u"Roxanne_2", u"Brielle_2", u"Tejeda_2")}));
ASSERT_EQ(2, persons->get_Count());
// إزالة شخص من المجموعة حسب الفهرس.
persons->RemoveAt(0);
ASSERT_EQ(1, persons->get_Count());
// إزالة جميع الأشخاص من المجموعة.
persons->Clear();
ASSERT_EQ(0, persons->get_Count());
```

## انظر أيضًا

* Class [PersonCollection](../)
* Namespace [Aspose::Words::Bibliography](../../)
* Library [Aspose.Words for C++](../../../)
