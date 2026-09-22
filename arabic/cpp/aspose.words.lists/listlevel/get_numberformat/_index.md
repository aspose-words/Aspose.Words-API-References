---
title: "طريقة Aspose::Words::Lists::ListLevel::get_NumberFormat"
linktitle: "get_NumberFormat"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Lists::ListLevel::get_NumberFormat. تُرجِع أو تُعيّن تنسيق الرقم لمستوى القائمة في C++."
type: docs
weight: 12000
url: /ar/cpp/aspose.words.lists/listlevel/get_numberformat/
---
## ListLevel::get_NumberFormat method


يعيد أو يضبط تنسيق الرقم للمستوى من القائمة.

```cpp
System::String Aspose::Words::Lists::ListLevel::get_NumberFormat() const
```

## ملاحظات


من بين أحرف النص العادية، يمكن أن يحتوي السلسلة على أحرف نائبة \x0000 إلى \x0008 تمثل الأرقام من مستويات القائمة المقابلة.

على سبيل المثال، السلسلة "\x0000.\x0001)" ستولد تسمية قائمة تشبه إلى حد ما "1.5)". الرقم "1" هو الرقم الحالي من المستوى الأول للقائمة، والرقم "5" هو الرقم الحالي من المستوى الثاني للقائمة.

القيمة Null غير مسموح بها، لكن السلسلة الفارغة التي تعني عدم وجود رقم صالحة.

## أمثلة



يوضح كيفية تطبيق تنسيق قائمة مخصص على الفقرات عند استخدام [DocumentBuilder](../../../aspose.words/documentbuilder/).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// تتيح لنا القائمة تنظيم وتزيين مجموعات الفقرات باستخدام رموز البادئة والمسافات البادئة.
// يمكننا إنشاء قوائم متداخلة بزيادة مستوى المسافة البادئة.
// يمكننا بدء وإنهاء قائمة باستخدام خاصية "ListFormat" لكائن Document Builder.
// كل فقرة نضيفها بين بداية القائمة ونهايتها ستصبح عنصرًا في القائمة.
// إنشاء قائمة من قالب Microsoft Word، وتخصيص أول مستويين من مستوياتها.
System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault);

System::SharedPtr<Aspose::Words::Lists::ListLevel> listLevel = list->get_ListLevels()->idx_get(0);
listLevel->get_Font()->set_Color(System::Drawing::Color::get_Red());
listLevel->get_Font()->set_Size(24);
listLevel->set_NumberStyle(Aspose::Words::NumberStyle::OrdinalText);
listLevel->set_StartAt(21);
listLevel->set_NumberFormat(u"\x0000");

listLevel->set_NumberPosition(-36);
listLevel->set_TextPosition(144);
listLevel->set_TabPosition(144);

listLevel = list->get_ListLevels()->idx_get(1);
listLevel->set_Alignment(Aspose::Words::Lists::ListLevelAlignment::Right);
listLevel->set_NumberStyle(Aspose::Words::NumberStyle::Bullet);
listLevel->get_Font()->set_Name(u"Wingdings");
listLevel->get_Font()->set_Color(System::Drawing::Color::get_Blue());
listLevel->get_Font()->set_Size(24);

// ستُنشئ قيمة NumberFormat هذه رموز تعداد نقطية على شكل نجمة.
listLevel->set_NumberFormat(u"\xf0af");
listLevel->set_TrailingCharacter(Aspose::Words::Lists::ListTrailingCharacter::Space);
listLevel->set_NumberPosition(144);

// إنشاء فقرات وتطبيق كلا مستويي القائمة من تنسيقنا المخصص علىها.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_ListFormat()->set_List(list);
builder->Writeln(u"The quick brown fox...");
builder->Writeln(u"The quick brown fox...");

builder->get_ListFormat()->ListIndent();
builder->Writeln(u"jumped over the lazy dog.");
builder->Writeln(u"jumped over the lazy dog.");

builder->get_ListFormat()->ListOutdent();
builder->Writeln(u"The quick brown fox...");

builder->get_ListFormat()->RemoveNumbers();

builder->get_Document()->Save(get_ArtifactsDir() + u"Lists.CreateCustomList.docx");
```


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
