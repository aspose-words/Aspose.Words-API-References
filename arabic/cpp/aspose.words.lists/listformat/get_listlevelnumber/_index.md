---
title: "طريقة Aspose::Words::Lists::ListFormat::get_ListLevelNumber"
linktitle: "get_ListLevelNumber"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Lists::ListFormat::get_ListLevelNumber. يحصل على أو يعيّن رقم مستوى القائمة (0 إلى 8) للفقرة في C++."
type: docs
weight: 7000
url: /ar/cpp/aspose.words.lists/listformat/get_listlevelnumber/
---
## ListFormat::get_ListLevelNumber method


يحصل أو يعيّن رقم مستوى القائمة (من 0 إلى 8) للفقرة.

```cpp
int32_t Aspose::Words::Lists::ListFormat::get_ListLevelNumber()
```

## ملاحظات


في مستندات Word، قد تتكون القوائم من مستوى واحد إلى تسعة مستويات، مرقمة من 0 إلى 8.

له تأثير فقط عندما تكون خاصية [List](../get_list/) مضبوطة للإشارة إلى قائمة صالحة.

## أمثلة



يظهر كيفية إنشاء قوائم نقطية ورقمية.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Aspose.Words main advantages are:");

// تتيح لنا القائمة تنظيم وتزيين مجموعات الفقرات باستخدام رموز البادئة والمسافات البادئة.
// يمكننا إنشاء قوائم متداخلة بزيادة مستوى المسافة البادئة.
// يمكننا بدء وإنهاء قائمة باستخدام خاصية "ListFormat" لكائن Document Builder.
// كل فقرة نضيفها بين بداية القائمة ونهايتها ستصبح عنصرًا في القائمة.
// فيما يلي نوعان من القوائم يمكننا إنشاؤهما باستخدام مُنشئ المستند.
// 1 -  قائمة نقطية:
// ستُطبق هذه القائمة مسافة بادئة ورمز نقطي ("•") قبل كل فقرة.
builder->get_ListFormat()->ApplyBulletDefault();
builder->Writeln(u"Great performance");
builder->Writeln(u"High reliability");
builder->Writeln(u"Quality code and working");
builder->Writeln(u"Wide variety of features");
builder->Writeln(u"Easy to understand API");

// إنهاء القائمة النقطية.
builder->get_ListFormat()->RemoveNumbers();

builder->InsertBreak(Aspose::Words::BreakType::ParagraphBreak);
builder->Writeln(u"Aspose.Words allows:");

// 2 -  قائمة مرقمة:
// القوائم المرقمة تُنشئ ترتيبًا منطقيًا للفقرات عن طريق ترقيم كل عنصر.
builder->get_ListFormat()->ApplyNumberDefault();

// هذه الفقرة هي العنصر الأول. سيحمل العنصر الأول في قائمة مرقمة الرمز \"1.\" كرمز للعنصر.
builder->Writeln(u"Opening documents from different formats:");

ASSERT_EQ(0, builder->get_ListFormat()->get_ListLevelNumber());

// استدعِ طريقة "ListIndent" لزيادة مستوى القائمة الحالي،
// والتي ستبدأ قائمة جديدة مستقلة، مع مسافة بادئة أعمق، عند العنصر الحالي من المستوى الأول للقائمة.
builder->get_ListFormat()->ListIndent();

ASSERT_EQ(1, builder->get_ListFormat()->get_ListLevelNumber());

// هذه هي العناصر الثلاثة الأولى من المستوى الثاني للقائمة، والتي ستحافظ على عدد
// مستقلاً عن عدد المستوى الأول للقائمة. وفقًا لتنسيق القائمة الحالي،
// سيكون لها رموز "a.", "b.", و "c.".
builder->Writeln(u"DOC");
builder->Writeln(u"PDF");
builder->Writeln(u"HTML");

// استدعِ طريقة "ListOutdent" للعودة إلى المستوى السابق للقائمة.
builder->get_ListFormat()->ListOutdent();

ASSERT_EQ(0, builder->get_ListFormat()->get_ListLevelNumber());

// سيستمر هذان الفقرتان في عدد المستوى الأول للقائمة.
// سيكون لهذه العناصر رموز "2.", و "3.".
builder->Writeln(u"Processing documents");
builder->Writeln(u"Saving documents in different formats:");

// إذا زدنا مستوى القائمة إلى مستوى أضفنا إليه عناصر مسبقًا،
// ستكون القائمة المتداخلة منفصلة عن السابقة، وسيبدأ ترقيمها من البداية.
// سيكون لهذه العناصر رموز "a.", "b.", "c.", "d.", و "e".
builder->get_ListFormat()->ListIndent();
builder->Writeln(u"DOC");
builder->Writeln(u"PDF");
builder->Writeln(u"HTML");
builder->Writeln(u"MHTML");
builder->Writeln(u"Plain text");

// خفض مستوى القائمة مرة أخرى.
builder->get_ListFormat()->ListOutdent();
builder->Writeln(u"Doing many other things!");

// إنهاء القائمة المرقمة.
builder->get_ListFormat()->RemoveNumbers();

doc->Save(get_ArtifactsDir() + u"Lists.ApplyDefaultBulletsAndNumbers.docx");
```


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

## انظر أيضًا

* Class [ListFormat](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
