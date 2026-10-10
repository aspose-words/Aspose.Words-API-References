---
title: "طريقة Aspose::Words::StyleCollection::Add"
linktitle: "Add"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::StyleCollection::Add. تنشئ نمطًا جديدًا معرفًا من قبل المستخدم وتضيفه إلى المجموعة في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words/stylecollection/add/
---
## StyleCollection::Add method


ينشئ نمطًا جديدًا معرفًا من قبل المستخدم ويضيفه إلى المجموعة.

```cpp
System::SharedPtr<Aspose::Words::Style> Aspose::Words::StyleCollection::Add(Aspose::Words::StyleType type, const System::String &name)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| type | Aspose::Words::StyleType | قيمة [StyleType](../../styletype/) التي تحدد نوع النمط المراد إنشاؤه. |
| name | const System::String\& | اسم النمط المراد إنشاؤه حسّاس لحالة الأحرف. |
## ملاحظات


يمكنك إنشاء نمط حرف، أو فقرة، أو قائمة.

عند إنشاء نمط قائمة، يتم إنشاء النمط بتنسيق قائمة مرقمة افتراضي (1 \\ a \\ i).

يرمي استثناءً إذا كان هناك نمط بهذا الاسم موجود بالفعل.

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


يوضح كيفية إضافة [Style](../../style/) إلى مجموعة أنماط المستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::StyleCollection> styles = doc->get_Styles();
// تعيين المعلمات الافتراضية للأنماط الجديدة التي قد نضيفها لاحقًا إلى هذه المجموعة.
styles->get_DefaultFont()->set_Name(u"Courier New");
// إذا أضفنا نمطًا من "StyleType.Paragraph"، فإن المجموعة ستطبق القيم الخاصة بـ
// خاصية "DefaultParagraphFormat" الخاصة به إلى خاصية "ParagraphFormat" للنمط.
styles->get_DefaultParagraphFormat()->set_FirstLineIndent(15.0);
// أضف نمطًا، ثم تحقق من أنه يحتوي على الإعدادات الافتراضية.
styles->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle");

ASSERT_EQ(u"Courier New", styles->idx_get(4)->get_Font()->get_Name());
ASPOSE_ASSERT_EQ(15.0, styles->idx_get(u"MyStyle")->get_ParagraphFormat()->get_FirstLineIndent());
```

## انظر أيضًا

* Class [Style](../../style/)
* Enum [StyleType](../../styletype/)
* Class [StyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
