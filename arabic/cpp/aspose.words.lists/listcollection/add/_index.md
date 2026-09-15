---
title: "طريقة Aspose::Words::Lists::ListCollection::Add"
linktitle: "Add"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Lists::ListCollection::Add. تنشئ قائمة جديدة بناءً على قالب مسبق التعريف وتضيفها إلى مجموعة القوائم في المستند في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.lists/listcollection/add/
---
## ListCollection::Add(Aspose::Words::Lists::ListTemplate) method


ينشئ قائمة جديدة بناءً على قالب محدد مسبقًا ويضيفها إلى مجموعة القوائم في المستند.

```cpp
System::SharedPtr<Aspose::Words::Lists::List> Aspose::Words::Lists::ListCollection::Add(Aspose::Words::Lists::ListTemplate listTemplate)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| listTemplate | Aspose::Words::Lists::ListTemplate | قالب القائمة. |

### ReturnValue

القائمة التي تم إنشاؤها حديثًا.
## ملاحظات


قوالب القوائم في Aspose.Words تتطابق مع 21 قالب قائمة متاحة في مربع الحوار النقاط والترقيم في Microsoft Word 2003.

جميع القوائم التي تم إنشاؤها باستخدام هذه الطريقة تحتوي على 9 مستويات للقائمة.

## أمثلة



يعرض كيفية العمل مع مستويات القوائم.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

ASSERT_FALSE(builder->get_ListFormat()->get_IsListItem());

// تتيح لنا القائمة تنظيم وتزيين مجموعات الفقرات باستخدام رموز البادئة والمسافات البادئة.
// يمكننا إنشاء قوائم متداخلة بزيادة مستوى المسافة البادئة.
// يمكننا بدء وإنهاء قائمة باستخدام خاصية "ListFormat" لكائن Document Builder.
// كل فقرة نضيفها بين بداية القائمة ونهايتها ستصبح عنصرًا في القائمة.
// فيما يلي نوعان من القوائم يمكننا إنشاؤهما باستخدام Document Builder.
// 1 -  قائمة مرقمة:
// القوائم المرقمة تُنشئ ترتيبًا منطقيًا للفقرات عن طريق ترقيم كل عنصر.
builder->get_ListFormat()->set_List(doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault));

ASSERT_TRUE(builder->get_ListFormat()->get_IsListItem());

// عن طريق ضبط الخاصية "ListLevelNumber"، يمكننا زيادة مستوى القائمة
// لبدء قائمة فرعية مستقلة عند عنصر القائمة الحالي.
// قالب القائمة في Microsoft Word المسمى "NumberDefault" يستخدم الأرقام لإنشاء مستويات القائمة للمستوى الأول.
// المستويات الأعمق للقائمة تستخدم الأحرف والأرقام الرومانية الصغيرة.
for (int32_t i = 0; i < 9; i++)
{
    builder->get_ListFormat()->set_ListLevelNumber(i);
    builder->Writeln(System::String(u"Level ") + i);
}

// 2 -  قائمة نقطية:
// ستُطبق هذه القائمة مسافة بادئة ورمز نقطي ("•") قبل كل فقرة.
// المستويات الأعمق لهذه القائمة ستستخدم رموزًا مختلفة، مثل "■" و "○".
builder->get_ListFormat()->set_List(doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::BulletDefault));

for (int32_t i = 0; i < 9; i++)
{
    builder->get_ListFormat()->set_ListLevelNumber(i);
    builder->Writeln(System::String(u"Level ") + i);
}

// يمكننا تعطيل تنسيق القوائم لتجنب تنسيق أي فقرات لاحقة كقوائم عن طريق إلغاء تعيين علامة "List".
builder->get_ListFormat()->set_List(nullptr);

ASSERT_FALSE(builder->get_ListFormat()->get_IsListItem());

doc->Save(get_ArtifactsDir() + u"Lists.SpecifyListLevel.docx");
```


يظهر كيفية إعادة بدء الترقيم في قائمة عن طريق نسخ القائمة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// تتيح لنا القائمة تنظيم وتزيين مجموعات الفقرات باستخدام رموز البادئة والمسافات البادئة.
// يمكننا إنشاء قوائم متداخلة بزيادة مستوى المسافة البادئة.
// يمكننا بدء وإنهاء قائمة باستخدام خاصية "ListFormat" لكائن Document Builder.
// كل فقرة نضيفها بين بداية القائمة ونهايتها ستصبح عنصرًا في القائمة.
// أنشئ قائمة من قالب Microsoft Word، وقم بتخصيص المستوى الأول للقائمة.
System::SharedPtr<Aspose::Words::Lists::List> list1 = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberArabicParenthesis);
list1->get_ListLevels()->idx_get(0)->get_Font()->set_Color(System::Drawing::Color::get_Red());
list1->get_ListLevels()->idx_get(0)->set_Alignment(Aspose::Words::Lists::ListLevelAlignment::Right);

// طبق قائمتنا على بعض الفقرات.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"List 1 starts below:");
builder->get_ListFormat()->set_List(list1);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");
builder->get_ListFormat()->RemoveNumbers();

// يمكننا إضافة نسخة من قائمة موجودة إلى مجموعة قوائم المستند
// لإنشاء قائمة مشابهة دون تعديل الأصل.
System::SharedPtr<Aspose::Words::Lists::List> list2 = doc->get_Lists()->AddCopy(list1);
list2->get_ListLevels()->idx_get(0)->get_Font()->set_Color(System::Drawing::Color::get_Blue());
list2->get_ListLevels()->idx_get(0)->set_StartAt(10);

// طبق القائمة الثانية على فقرات جديدة.
builder->Writeln(u"List 2 starts below:");
builder->get_ListFormat()->set_List(list2);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");
builder->get_ListFormat()->RemoveNumbers();

doc->Save(get_ArtifactsDir() + u"Lists.RestartNumberingUsingListCopy.docx");
```


يوضح كيفية إنشاء قائمة عن طريق تطبيق تنسيق قائمة جديد على مجموعة من الفقرات.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Paragraph 1");
builder->Writeln(u"Paragraph 2");
builder->Write(u"Paragraph 3");

System::SharedPtr<Aspose::Words::NodeCollection> paras = doc->GetChildNodes(Aspose::Words::NodeType::Paragraph, true);

ASSERT_EQ(0, paras->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> n)>>([](System::SharedPtr<Aspose::Words::Node> n) -> bool
{
    return (System::ExplicitCast<Aspose::Words::Paragraph>(n))->get_ListFormat()->get_IsListItem();
}))));

System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberUppercaseLetterDot);

for (auto&& paragraph : System::IterateOver(paras->LINQ_OfType<System::SharedPtr<Aspose::Words::Paragraph> >()))
{
    paragraph->get_ListFormat()->set_List(list);
    paragraph->get_ListFormat()->set_ListLevelNumber(1);
}

ASSERT_EQ(3, paras->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> n)>>([](System::SharedPtr<Aspose::Words::Node> n) -> bool
{
    return (System::ExplicitCast<Aspose::Words::Paragraph>(n))->get_ListFormat()->get_IsListItem();
}))));
```

## انظر أيضًا

* Class [List](../../list/)
* Enum [ListTemplate](../../listtemplate/)
* Class [ListCollection](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
## ListCollection::Add(const System::SharedPtr\<Aspose::Words::Style\>\&) method


ينشئ قائمة جديدة تشير إلى نمط قائمة ويضيفها إلى مجموعة القوائم في المستند.

```cpp
System::SharedPtr<Aspose::Words::Lists::List> Aspose::Words::Lists::ListCollection::Add(const System::SharedPtr<Aspose::Words::Style> &listStyle)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| listStyle | const System::SharedPtr\<Aspose::Words::Style\>\& | نمط القائمة. |

### ReturnValue

القائمة التي تم إنشاؤها حديثًا.
## ملاحظات


القائمة التي تم إنشاؤها حديثًا تشير إلى نمط القائمة. إذا قمت بتغيير خصائص نمط القائمة، فإنها تنعكس في خصائص القائمة. والعكس بالعكس، إذا قمت بتغيير خصائص القائمة، فإنها تنعكس في خصائص نمط القائمة.

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

* Class [List](../../list/)
* Class [Style](../../../aspose.words/style/)
* Class [ListCollection](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
