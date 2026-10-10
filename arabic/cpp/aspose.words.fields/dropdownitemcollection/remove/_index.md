---
title: "Aspose::Words::Fields::DropDownItemCollection::Remove طريقة"
linktitle: "Remove"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Fields::DropDownItemCollection::Remove طريقة. يزيل القيمة المحددة من المجموعة في C++."
type: docs
weight: 17000
url: /ar/cpp/aspose.words.fields/dropdownitemcollection/remove/
---
## DropDownItemCollection::Remove method


يزيل القيمة المحددة من المجموعة.

```cpp
void Aspose::Words::Fields::DropDownItemCollection::Remove(const System::String &name)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| name | const System::String\& | القيمة الحساسة لحالة الأحرف التي يجب إزالتها. |

## أمثلة



يوضح كيفية إدراج حقل مربع اختيار، وتعديل العناصر في مجموعة عناصره.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// أدرج مربع اختيار، ثم تحقق من مجموعة العناصر المنسدلة الخاصة به.
// في Microsoft Word، سيقوم المستخدم بالنقر على مربع الاختيار،
// ثم يختار أحد عناصر النص في المجموعة للعرض.
System::ArrayPtr<System::String> items = System::MakeArray<System::String>({u"One", u"Two", u"Three"});
System::SharedPtr<Aspose::Words::Fields::FormField> comboBoxField = builder->InsertComboBox(u"DropDown", items, 0);
System::SharedPtr<Aspose::Words::Fields::DropDownItemCollection> dropDownItems = comboBoxField->get_DropDownItems();

ASSERT_EQ(3, dropDownItems->get_Count());
ASSERT_EQ(u"One", dropDownItems->idx_get(0));
ASSERT_EQ(1, dropDownItems->IndexOf(u"Two"));
ASSERT_TRUE(dropDownItems->Contains(u"Three"));

// هناك طريقتان لإضافة عنصر جديد إلى مجموعة موجودة من عناصر صندوق القائمة المنسدلة.
// 1 - أضف عنصرًا إلى نهاية المجموعة:
dropDownItems->Add(u"Four");

// 2 - أدخل عنصرًا قبل عنصر آخر عند فهرس محدد:
dropDownItems->Insert(3, u"Three and a half");

ASSERT_EQ(5, dropDownItems->get_Count());

// تكرار عبر المجموعة وطباعة كل عنصر.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::String>> dropDownCollectionEnumerator = dropDownItems->GetEnumerator();
    while (dropDownCollectionEnumerator->MoveNext())
    {
        std::cout << dropDownCollectionEnumerator->get_Current() << std::endl;
    }
}

// هناك طريقتان لإزالة العناصر من مجموعة العناصر المنسدلة.
// 1 - أزل عنصرًا يحتوي على محتوى يساوي السلسلة الممررة:
dropDownItems->Remove(u"Four");

// 2 - أزل عنصرًا عند فهرس:
dropDownItems->RemoveAt(3);

ASSERT_EQ(3, dropDownItems->get_Count());
ASSERT_FALSE(dropDownItems->Contains(u"Three and a half"));
ASSERT_FALSE(dropDownItems->Contains(u"Four"));

doc->Save(get_ArtifactsDir() + u"FormFields.DropDownItemCollection.html");

// افرغ المجموعة بالكامل من العناصر المنسدلة.
dropDownItems->Clear();
```

## انظر أيضًا

* Class [DropDownItemCollection](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
