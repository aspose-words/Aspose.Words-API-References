---
title: "Aspose::Words::Markup::CustomXmlPropertyCollection فئة"
linktitle: "CustomXmlPropertyCollection"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Markup::CustomXmlPropertyCollection فئة. تمثل مجموعة من سمات XML المخصصة أو خصائص العلامات الذكية. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 6000
url: /ar/cpp/aspose.words.markup/customxmlpropertycollection/
---
## CustomXmlPropertyCollection class


يمثل مجموعة من سمات XML مخصصة أو خصائص العلامة الذكية. لمعرفة المزيد، قم بزيارة مقالة الوثائق [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/).

```cpp
class CustomXmlPropertyCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Markup::CustomXmlProperty>>
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::Markup::CustomXmlProperty\>\&) | يضيف خاصية إلى المجموعة. |
| [Clear](./clear/)() | يزيل جميع العناصر من المجموعة. |
| [Contains](./contains/)(const System::String\&) | يحدد ما إذا كانت المجموعة تحتوي على خاصية بالاسم المعطى. |
| [get_Count](./get_count/)() | يحصل على عدد العناصر الموجودة في المجموعة. |
| [GetEnumerator](./getenumerator/)() override | يرجع كائن عداد يمكن استخدامه للتنقل عبر جميع العناصر في المجموعة. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(const System::String\&) | يحصل على خاصية بالاسم المحدد. |
| [idx_get](./idx_get/)(int32_t) | يحصل على خاصية في الفهرس المحدد. |
| [IndexOfKey](./indexofkey/)(const System::String\&) | يرجع الفهرس الصفري للخاصية المحددة في المجموعة. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::String\&) | يزيل خاصية بالاسم المحدد من المجموعة. |
| [RemoveAt](./removeat/)(int32_t) | يزيل خاصية في الفهرس المحدد. |
| static [Type](./type/)() |  |
## ملاحظات


العناصر هي كائنات [CustomXmlProperty](../customxmlproperty/).

## أمثلة



يوضح كيفية العمل مع خصائص العلامات الذكية للحصول على معلومات متعمقة حول العلامات الذكية.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Smart tags.doc");

// تظهر علامة ذكية في مستند مع Microsoft Word يتعرف على جزء من نصها كنوع من البيانات،
// مثل اسم أو تاريخ أو عنوان، ويحولها إلى ارتباط تشعبي يعرض خطًا سفليًا نقطيًا أرجوانيًا.
// في Word 2003، يمكننا تمكين العلامات الذكية عبر "Tools" -> "AutoCorrect options..." -> "SmartTags".
// في مستند الإدخال الخاص بنا، هناك ثلاثة كائنات سجلتها Microsoft Word كعلامات ذكية.
// قد تكون العلامات الذكية متداخلة، لذا تحتوي هذه المجموعة على المزيد.
System::ArrayPtr<System::SharedPtr<Aspose::Words::Markup::SmartTag>> smartTags = doc->GetChildNodes(Aspose::Words::NodeType::SmartTag, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Markup::SmartTag> >()->LINQ_ToArray();

ASSERT_EQ(8, smartTags->get_Length());

// العضو "Properties" في علامة ذكية يحتوي على بيانات التعريف الخاصة بها، والتي ستكون مختلفة لكل نوع من العلامات الذكية.
// خصائص علامة ذكية من نوع "date" تحتوي على السنة والشهر واليوم.
System::SharedPtr<Aspose::Words::Markup::CustomXmlPropertyCollection> properties = smartTags[7]->get_Properties();

ASSERT_EQ(4, properties->get_Count());

{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Markup::CustomXmlProperty>>> enumerator = properties->GetEnumerator();
    while (enumerator->MoveNext())
    {
        std::cout << System::String::Format(u"Property name: {0}, value: {1}", enumerator->get_Current()->get_Name(), enumerator->get_Current()->get_Value()) << std::endl;
        ASSERT_EQ(u"", enumerator->get_Current()->get_Uri());
    }
}

// يمكننا أيضًا الوصول إلى الخصائص بطرق مختلفة، مثل زوج المفتاح-القيمة.
ASSERT_TRUE(properties->Contains(u"Day"));
ASSERT_EQ(u"22", properties->idx_get(u"Day")->get_Value());
ASSERT_EQ(u"2003", properties->idx_get(2)->get_Value());
ASSERT_EQ(1, properties->IndexOfKey(u"Month"));

// فيما يلي ثلاث طرق لإزالة العناصر من مجموعة الخصائص.
// 1 -  إزالة حسب الفهرس:
properties->RemoveAt(3);

ASSERT_EQ(3, properties->get_Count());

// 2 -  إزالة حسب الاسم:
properties->Remove(u"Year");

ASSERT_EQ(2, properties->get_Count());

// 3 - مسح المجموعة بالكامل مرة واحدة:
properties->Clear();

ASSERT_EQ(0, properties->get_Count());
```

## انظر أيضًا

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
