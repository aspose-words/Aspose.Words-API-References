---
title: "طريقة Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreDeleted"
linktitle: "get_IgnoreDeleted"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreDeleted. يحصل أو يضبط قيمة منطقية تشير إلى ما إذا كان يجب تجاهل النص داخل مراجعات الحذف. القيمة الافتراضية هي false في C++."
type: docs
weight: 7000
url: /ar/cpp/aspose.words.replacing/findreplaceoptions/get_ignoredeleted/
---
## FindReplaceOptions::get_IgnoreDeleted method


يحصل أو يعيّن قيمة منطقية تشير إلى ما إذا كان يجب تجاهل النص داخل مراجعات الحذف. القيمة الافتراضية هي **false**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreDeleted() const
```


## أمثلة



يظهر كيفية تضمين أو تجاهل النص داخل مراجعات الحذف أثناء عملية البحث والاستبدال.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");
builder->Writeln(u"Hello again!");

// ابدأ تتبع المراجعات وأزل الفقرة الثانية، مما سيخلق مراجعة حذف.
// ستستمر تلك الفقرة في المستند حتى نقبل مراجعة الحذف.
doc->StartTrackRevisions(u"John Doe", System::DateTime::get_Now());
doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(1)->Remove();
doc->StopTrackRevisions();

ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(1)->get_IsDeleteRevision());

// يمكننا استخدام كائن "FindReplaceOptions" لتعديل عملية البحث والاستبدال.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// قم بتعيين علامة "IgnoreDeleted" إلى "true" للحصول على عملية البحث والاستبدال
// لتجاهل الفقرات التي هي مراجعات حذف.
// قم بتعيين علامة "IgnoreDeleted" إلى "false" للحصول على عملية البحث والاستبدال
// للبحث أيضًا عن النص داخل مراجعات الحذف.
options->set_IgnoreDeleted(ignoreTextInsideDeleteRevisions);

doc->get_Range()->Replace(u"Hello", u"Greetings", options);

ASSERT_EQ(ignoreTextInsideDeleteRevisions ? System::String(u"Greetings world!\rHello again!") : System::String(u"Greetings world!\rGreetings again!"), doc->GetText().Trim());
```

## انظر أيضًا

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
