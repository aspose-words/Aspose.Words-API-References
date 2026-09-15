---
title: "Aspose::Words::Lists::ListLevel::get_RestartAfterLevel method"
linktitle: "get_RestartAfterLevel"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Lists::ListLevel::get_RestartAfterLevel method. يحدد أو يرجع مستوى القائمة الذي يجب أن يظهر قبل أن يبدأ المستوى المحدد إعادة ترقيم في C++."
type: docs
weight: 15000
url: /ar/cpp/aspose.words.lists/listlevel/get_restartafterlevel/
---
## ListLevel::get_RestartAfterLevel method


يضبط أو يعيد المستوى الذي يجب أن يظهر قبل المستوى المحدد لإعادة بدء الترقيم.

```cpp
int32_t Aspose::Words::Lists::ListLevel::get_RestartAfterLevel() const
```

## ملاحظات


القيمة -1 تعني أن الترقيم سيستمر.

## أمثلة



يعرض طرقًا متقدمة لتخصيص تسميات القوائم.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// تتيح لنا القائمة تنظيم وتزيين مجموعات الفقرات باستخدام رموز البادئة والمسافات البادئة.
// يمكننا إنشاء قوائم متداخلة بزيادة مستوى المسافة البادئة.
// يمكننا بدء وإنهاء قائمة باستخدام خاصية "ListFormat" لكائن Document Builder.
// كل فقرة نضيفها بين بداية القائمة ونهايتها ستصبح عنصرًا في القائمة.
System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault);

// ستُنسق تسميات المستوى 1 وفق نمط الفقرة "Heading 1" وستحتوي على بادئة.
// ستظهر بهذه الصيغة مثل "Appendix A"، "Appendix B"...
list->get_ListLevels()->idx_get(0)->set_NumberFormat(u"Appendix \x0000");
list->get_ListLevels()->idx_get(0)->set_NumberStyle(Aspose::Words::NumberStyle::UppercaseLetter);
list->get_ListLevels()->idx_get(0)->set_LinkedStyle(doc->get_Styles()->idx_get(u"Heading 1"));

// ستعرض تسميات المستوى 2 الأرقام الحالية للمستوى الأول والثاني من القائمة وستحتوي على أصفار بادئة.
// إذا كان المستوى الأول للقائمة هو 1، فإن تسميات القائمة من هذه ستظهر مثل "Section (1.01)", "Section (1.02)"...
list->get_ListLevels()->idx_get(1)->set_NumberFormat(u"Section (\x0000" u".\x0001" u")");
list->get_ListLevels()->idx_get(1)->set_NumberStyle(Aspose::Words::NumberStyle::LeadingZero);

// لاحظ أن المستوى الأعلى يستخدم ترقيم UppercaseLetter.
// يمكننا تعيين الخاصية "IsLegal" لاستخدام أرقام عربية للمستويات العليا من القائمة.
list->get_ListLevels()->idx_get(1)->set_IsLegal(true);
list->get_ListLevels()->idx_get(1)->set_RestartAfterLevel(0);

// ستكون تسميات المستوى 3 أرقامًا رومانية كبيرة مع بادئة ولاحقة، وستُعاد بدءها عند كل عنصر من المستوى 1 في القائمة.
// ستظهر تسميات القائمة هذه مثل "-I-", "-II-"...
list->get_ListLevels()->idx_get(2)->set_NumberFormat(u"-\x0002" u"-");
list->get_ListLevels()->idx_get(2)->set_NumberStyle(Aspose::Words::NumberStyle::UppercaseRoman);
list->get_ListLevels()->idx_get(2)->set_RestartAfterLevel(1);

// اجعل تسميات جميع مستويات القائمة غامقة.
for (auto&& level : list->get_ListLevels())
{
    level->get_Font()->set_Bold(true);
}

// طبق تنسيق القائمة على الفقرة الحالية.
builder->get_ListFormat()->set_List(list);

// إنشاء عناصر قائمة ستعرض جميع المستويات الثلاثة لقائمتنا.
for (int32_t n = 0; n < 2; n++)
{
    for (int32_t i = 0; i < 3; i++)
    {
        builder->get_ListFormat()->set_ListLevelNumber(i);
        builder->Writeln(System::String(u"Level ") + i);
    }
}

builder->get_ListFormat()->RemoveNumbers();

doc->Save(get_ArtifactsDir() + u"Lists.CreateListRestartAfterHigher.docx");
```

## انظر أيضًا

* Class [ListLevel](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
