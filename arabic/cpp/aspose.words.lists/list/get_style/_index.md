---
title: "Aspose::Words::Lists::List::get_Style طريقة"
linktitle: "get_Style"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Lists::List::get_Style طريقة. يحصل على نمط القائمة الذي تشير إليه هذه القائمة أو تعرفه في C++."
type: docs
weight: 11000
url: /ar/cpp/aspose.words.lists/list/get_style/
---
## List::get_Style method


يحصل على نمط القائمة الذي تشير إليه هذه القائمة أو تعرفه.

```cpp
System::SharedPtr<Aspose::Words::Style> Aspose::Words::Lists::List::get_Style()
```

## ملاحظات


إذا لم تكن هذه القائمة مرتبطة بنمط قائمة، فستعيد الخاصية **null**.

قد تكون القائمة إشارة إلى نمط قائمة، في هذه الحالة سيكون [IsListStyleReference](../get_isliststylereference/) **true**.

قد تكون القائمة تعريفًا لنمط قائمة، في هذه الحالة سيكون [IsListStyleDefinition](../get_isliststyledefinition/) **true**. لا يمكن تطبيق مثل هذه القائمة على الفقرات في المستند مباشرة.

## أمثلة



يظهر كيفية إنشاء نمط قائمة واستخدامه في مستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// تتيح لنا القائمة تنظيم وتزيين مجموعات الفقرات باستخدام رموز البادئة والمسافات البادئة.
// يمكننا إنشاء قوائم متداخلة بزيادة مستوى المسافة البادئة.
// يمكننا بدء وإنهاء قائمة باستخدام خاصية "ListFormat" لكائن Document Builder.
// كل فقرة نضيفها بين بداية القائمة ونهايتها ستصبح عنصرًا في القائمة.
// يمكننا احتواء كائن List كامل داخل نمط.
System::SharedPtr<Aspose::Words::Style> listStyle = doc->get_Styles()->Add(Aspose::Words::StyleType::List, u"MyListStyle");

System::SharedPtr<Aspose::Words::Lists::List> list1 = listStyle->get_List();

ASSERT_TRUE(list1->get_IsListStyleDefinition());
ASSERT_FALSE(list1->get_IsListStyleReference());
ASSERT_TRUE(list1->get_IsMultiLevel());
ASPOSE_ASSERT_EQ(listStyle, list1->get_Style());

// غيّر مظهر جميع مستويات القائمة في قائمتنا.
for (auto&& level : list1->get_ListLevels())
{
    level->get_Font()->set_Name(u"Verdana");
    level->get_Font()->set_Color(System::Drawing::Color::get_Blue());
    level->get_Font()->set_Bold(true);
}

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Using list style first time:");

// أنشئ قائمة أخرى من قائمة داخل نمط.
System::SharedPtr<Aspose::Words::Lists::List> list2 = doc->get_Lists()->Add(listStyle);

ASSERT_FALSE(list2->get_IsListStyleDefinition());
ASSERT_TRUE(list2->get_IsListStyleReference());
ASPOSE_ASSERT_EQ(listStyle, list2->get_Style());

// أضف بعض عناصر القائمة التي ستقوم قائمتنا بتنسيقها.
builder->get_ListFormat()->set_List(list2);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");
builder->get_ListFormat()->RemoveNumbers();

builder->Writeln(u"Using list style second time:");

// إنشاء وتطبيق قائمة أخرى بناءً على نمط القائمة.
System::SharedPtr<Aspose::Words::Lists::List> list3 = doc->get_Lists()->Add(listStyle);
builder->get_ListFormat()->set_List(list3);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");
builder->get_ListFormat()->RemoveNumbers();

builder->get_Document()->Save(get_ArtifactsDir() + u"Lists.CreateAndUseListStyle.docx");
```

## انظر أيضًا

* Class [Style](../../../aspose.words/style/)
* Class [List](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
