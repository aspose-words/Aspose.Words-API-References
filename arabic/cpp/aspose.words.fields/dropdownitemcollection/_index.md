---
title: "Aspose::Words::Fields::DropDownItemCollection فئة"
linktitle: "DropDownItemCollection"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Fields::DropDownItemCollection فئة. مجموعة من السلاسل تمثل جميع العناصر في حقل نموذج منسدلة. للتعرف على المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words.fields/dropdownitemcollection/
---
## DropDownItemCollection class


مجموعة من السلاسل التي تمثل جميع العناصر في حقل نموذج منسدلة. لمعرفة المزيد، زر مقالة الوثائق [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class DropDownItemCollection : public System::Collections::Generic::IEnumerable<System::String>,
                               public Aspose::Words::IComplexAttr
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [Add](./add/)(const System::String\&) | يضيف سلسلة إلى نهاية المجموعة. |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Clear](./clear/)() | يزيل جميع العناصر من المجموعة. |
| [Contains](./contains/)(const System::String\&) | يحدد ما إذا كانت المجموعة تحتوي على القيمة المحددة. |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | يحصل على عدد العناصر الموجودة في المجموعة. |
| [GetEnumerator](./getenumerator/)() override | يرجع كائن عداد يمكن استخدامه للتنقل عبر جميع العناصر في المجموعة. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | يحصل أو يضبط العنصر في الفهرس المحدد. |
| [idx_set](./idx_set/)(int32_t, const System::String\&) | يحصل أو يضبط العنصر في الفهرس المحدد. |
| [IndexOf](./indexof/)(const System::String\&) | يرجع الفهرس الصفري للقيمة المحددة في المجموعة. |
| [Insert](./insert/)(int32_t, const System::String\&) | يدرج سلسلة في المجموعة عند الفهرس المحدد. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::String\&) | يزيل القيمة المحددة من المجموعة. |
| [RemoveAt](./removeat/)(int32_t) | يزيل قيمة عند الفهرس المحدد. |
| static [Type](./type/)() |  |
| [virtualizeBeginConstIterator](./virtualizebeginconstiterator/)() const override |  |
| [virtualizeBeginIterator](./virtualizebeginiterator/)() override |  |
| [virtualizeEndConstIterator](./virtualizeendconstiterator/)() const override |  |
| [virtualizeEndIterator](./virtualizeenditerator/)() override |  |
## Typedefs

| تعريف نوع | الوصف |
| --- | --- |
| [const_iterator](./const_iterator/) |  |
| [iterator](./iterator/) |  |
| [iterator_holder_type](./iterator_holder_type/) |  |
| [virtualized_iterator](./virtualized_iterator/) |  |
| [virtualized_iterator_element](./virtualized_iterator_element/) |  |

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

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
