---
title: "Aspose::Words::Markup::CustomXmlProperty::get_Uri طريقة"
linktitle: "get_Uri"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Markup::CustomXmlProperty::get_Uri طريقة. يحصل على أو يضبط URI مساحة الاسم للخاصية المخصصة XML أو خاصية العلامة الذكية في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words.markup/customxmlproperty/get_uri/
---
## CustomXmlProperty::get_Uri method


يحصل أو يضبط URI مساحة الاسم لسمة XML المخصصة أو خاصية الوسم الذكي.

```cpp
System::String Aspose::Words::Markup::CustomXmlProperty::get_Uri() const
```

## ملاحظات


لا يمكن أن تكون **null**.

القيمة الافتراضية هي سلسلة فارغة.

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

* Class [CustomXmlProperty](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
