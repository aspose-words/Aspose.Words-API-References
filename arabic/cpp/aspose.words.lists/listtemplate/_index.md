---
title: "Aspose::Words::Lists::ListTemplate enum"
linktitle: "ListTemplate"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Lists::ListTemplate enum. يحدد أحد تنسيقات القوائم المعرفة مسبقًا المتاحة في Microsoft Word بلغة C++."
type: docs
weight: 8000
url: /ar/cpp/aspose.words.lists/listtemplate/
---
## ListTemplate enum


يحدد أحد تنسيقات القوائم المعرفة مسبقًا المتوفرة في Microsoft Word.

```cpp
enum class ListTemplate
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| BulletDefault | 0 | قائمة نقطية افتراضية بـ 9 مستويات. نقطة المستوى الأول هي قرص، نقطة المستوى الثاني هي دائرة، نقطة المستوى الثالث هي مربع. ثم يتكرر التنسيق للمستويات المتبقية. كل مستوى مُزاح إلى اليمين بمقدار 0.25" مقارنةً بالمستوى السابق. يتطابق مع قالب القائمة النقطية الأول في مربع الحوار "Bullets and Numbering" في Microsoft Word. |
| BulletDisk | n/a | نفسه مثل [BulletDefault](./). يتطابق مع قالب القائمة النقطية الأول في مربع الحوار "Bullets and Numbering" في Microsoft Word. |
| BulletCircle | n/a | نقطة المستوى الأول هي دائرة. المستويات المتبقية هي نفسها كما في [BulletDefault](./). يتطابق مع قالب القائمة النقطية الثاني في مربع الحوار "Bullets and Numbering" في Microsoft Word. |
| BulletSquare | n/a | نقطة المستوى الأول هي مربع. المستويات المتبقية هي نفسها كما في [BulletDefault](./). يتطابق مع قالب القائمة النقطية الثالث في مربع الحوار "Bullets and Numbering" في Microsoft Word. |
| BulletDiamonds | n/a | نقطة المستوى الأول هي حرف Wingding ماسي رباعي. المستويات المتبقية هي نفسها كما في [BulletDefault](./). يتطابق مع قالب القائمة النقطية الخامس في مربع الحوار "Bullets and Numbering" في Microsoft Word. |
| BulletArrowHead | n/a | نقطة المستوى الأول هي حرف Wingding على شكل رأس سهم. المستويات المتبقية هي نفسها كما في [BulletDefault](./). يتطابق مع قالب القائمة النقطية السادس في مربع الحوار "Bullets and Numbering" في Microsoft Word. |
| BulletTick | n/a | نقطة المستوى الأول هي حرف Wingding على شكل علامة اختيار. المستويات المتبقية هي نفسها كما في [BulletDefault](./). يتطابق مع قالب القائمة النقطية السابع في مربع الحوار "Bullets and Numbering" في Microsoft Word. |
| NumberDefault | n/a | قائمة مرقمة افتراضية بـ 9 مستويات. ترقيم عربي (1., 2., 3., ...) للمستوى الأول، ترقيم بحروف صغيرة (a., b., c., ...) للمستوى الثاني، ترقيم روماني بحروف صغيرة (i., ii., iii., ...) للمستوى الثالث. ثم يتكرر التنسيق للمستويات المتبقية. كل مستوى مُزاح إلى اليمين بمقدار 0.25" مقارنةً بالمستوى السابق. يتطابق مع قالب القائمة المرقمة الأول في مربع الحوار "Bullets and Numbering" في Microsoft Word. |
| NumberArabicDot | n/a | نفسه مثل [NumberDefault](./). يتطابق مع قالب القائمة المرقمة الأول في مربع الحوار "Bullets and Numbering" في Microsoft Word. |
| NumberArabicParenthesis | n/a | رقم المستوى الأول هو "1)". المستويات المتبقية هي نفسها كما في [NumberDefault](./). يتطابق مع قالب القائمة المرقمة الثاني في مربع الحوار "Bullets and Numbering" في Microsoft Word. |
| NumberUppercaseRomanDot | n/a | رقم المستوى الأول هو "I.". المستويات المتبقية هي نفسها كما في [NumberDefault](./). يتطابق مع قالب القائمة المرقمة الثالث في مربع الحوار "Bullets and Numbering" في Microsoft Word. |
| NumberUppercaseLetterDot | n/a | رقم المستوى الأول هو "A.". المستويات المتبقية هي نفسها كما في [NumberDefault](./). يتطابق مع قالب القائمة المرقمة الرابع في مربع الحوار "Bullets and Numbering" في Microsoft Word. |
| NumberLowercaseLetterParenthesis | n/a | رقم المستوى الأول هو "a)". المستويات المتبقية هي نفسها كما في [NumberDefault](./). يتطابق مع قالب القائمة المرقمة الخامس في مربع الحوار "Bullets and Numbering" في Microsoft Word. |
| NumberLowercaseLetterDot | n/a | رقم المستوى الأول هو "a.". المستويات المتبقية هي نفسها كما في [NumberDefault](./). يتطابق مع قالب القائمة المرقمة السادس في مربع الحوار النقاط والترقيم في Microsoft Word. |
| NumberLowercaseRomanDot | n/a | رقم المستوى الأول هو "i.". المستويات المتبقية هي نفسها كما في [NumberDefault](./). يتطابق مع قالب القائمة المرقمة السابع في مربع الحوار النقاط والترقيم في Microsoft Word. |
| OutlineNumbers | n/a | قائمة مخطط بمستويات مرقمة "1), a), i), (1), (a), (i), 1., a., i.". يتطابق مع قالب القائمة المخططة الأول في مربع الحوار النقاط والترقيم في Microsoft Word. |
| OutlineLegal | n/a | قائمة مخطط بمستويات مرقمة "1., 1.1., 1.1.1, ...". يتطابق مع قالب القائمة المخططة الثاني في مربع الحوار النقاط والترقيم في Microsoft Word. |
| OutlineBullets | n/a | قوائم مخطط مع نقاط مختلفة لمستويات مختلفة. يتطابق مع قالب القائمة المخططة الثالث في مربع الحوار النقاط والترقيم في Microsoft Word. |
| OutlineHeadingsArticleSection | n/a | قائمة مخطط بمستويات مرتبطة بأنماط العناوين. يتطابق مع قالب القائمة المخططة الرابع في مربع الحوار النقاط والترقيم في Microsoft Word. |
| OutlineHeadingsLegal | n/a | قائمة مخطط بمستويات مرتبطة بأنماط العناوين. يتطابق مع قالب القائمة المخططة الخامس في مربع الحوار النقاط والترقيم في Microsoft Word. |
| OutlineHeadingsNumbers | n/a | قائمة مخطط بمستويات مرتبطة بأنماط العناوين. يتطابق مع قالب القائمة المخططة السادس في مربع الحوار النقاط والترقيم في Microsoft Word. |
| OutlineHeadingsChapter | n/a | قائمة مخطط بمستويات مرتبطة بأنماط العناوين. يتطابق مع قالب القائمة المخططة السابع في مربع الحوار النقاط والترقيم في Microsoft Word. |

## ملاحظات


يتم استخدام قيمة قالب القائمة كمعامل في طريقة [Add()](../listcollection/add/).

قوالب القوائم في Aspose.Words تتطابق مع 21 قالب قائمة متاحة في مربع الحوار النقاط والترقيم في Microsoft Word 2003.

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

## انظر أيضًا

* Namespace [Aspose::Words::Lists](../)
* Library [Aspose.Words for C++](../../)
