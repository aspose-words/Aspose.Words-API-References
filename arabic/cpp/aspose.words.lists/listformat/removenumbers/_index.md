---
title: "طريقة Aspose::Words::Lists::ListFormat::RemoveNumbers"
linktitle: "RemoveNumbers"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Lists::ListFormat::RemoveNumbers. يزيل الأرقام أو الرموز النقطية من الفقرة الحالية ويضبط مستوى القائمة إلى الصفر في C++."
type: docs
weight: 12000
url: /ar/cpp/aspose.words.lists/listformat/removenumbers/
---
## ListFormat::RemoveNumbers method


يزيل الأرقام أو النقاط من الفقرة الحالية ويضبط مستوى القائمة إلى الصفر.

```cpp
void Aspose::Words::Lists::ListFormat::RemoveNumbers()
```

## ملاحظات


استدعاء هذه الطريقة يعادل ضبط الخاصية [List](../get_list/) إلى **null**.

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


يظهر كيفية إزالة تنسيق القائمة من جميع الفقرات في النص الرئيسي لقسم.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_ListFormat()->ApplyNumberDefault();
builder->Writeln(u"Numbered list item 1");
builder->Writeln(u"Numbered list item 2");
builder->Writeln(u"Numbered list item 3");
builder->get_ListFormat()->RemoveNumbers();

System::SharedPtr<Aspose::Words::NodeCollection> paras = doc->GetChildNodes(Aspose::Words::NodeType::Paragraph, true);
ASSERT_EQ(3, paras->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> n)>>([](System::SharedPtr<Aspose::Words::Node> n) -> bool
{
    return (System::ExplicitCast<Aspose::Words::Paragraph>(n))->get_ListFormat()->get_IsListItem();
}))));

for (auto&& paragraph : System::IterateOver<Aspose::Words::Paragraph>(paras))
{
    paragraph->get_ListFormat()->RemoveNumbers();
}

ASSERT_EQ(0, paras->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> n)>>([](System::SharedPtr<Aspose::Words::Node> n) -> bool
{
    return (System::ExplicitCast<Aspose::Words::Paragraph>(n))->get_ListFormat()->get_IsListItem();
}))));
```

## انظر أيضًا

* Class [ListFormat](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
