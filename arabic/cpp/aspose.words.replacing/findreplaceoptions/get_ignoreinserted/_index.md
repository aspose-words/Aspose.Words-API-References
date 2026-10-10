---
title: "طريقة Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreInserted"
linktitle: "get_IgnoreInserted"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreInserted. يحصل أو يعيّن قيمة منطقية تشير إلى ما إذا كان يجب تجاهل النص داخل مراجعات الإدراج. القيمة الافتراضية هي false في C++."
type: docs
weight: 11000
url: /ar/cpp/aspose.words.replacing/findreplaceoptions/get_ignoreinserted/
---
## FindReplaceOptions::get_IgnoreInserted method


يحصل أو يعيّن قيمة منطقية تشير إلى ما إذا كان يجب تجاهل النص داخل مراجعات الإدراج. القيمة الافتراضية هي **false**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreInserted() const
```


## أمثلة



يوضح كيفية تضمين أو تجاهل النص داخل مراجعات الإدراج أثناء عملية البحث والاستبدال.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");

// ابدأ تتبع المراجعات وأدرج فقرة. ستكون تلك الفقرة مراجعة إدراج.
doc->StartTrackRevisions(u"John Doe", System::DateTime::get_Now());
builder->Writeln(u"Hello again!");
doc->StopTrackRevisions();

ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(1)->get_IsInsertRevision());

// يمكننا استخدام كائن "FindReplaceOptions" لتعديل عملية البحث والاستبدال.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// عيّن علامة "IgnoreInserted" إلى "true" للحصول على عملية البحث والاستبدال
// لتجاهل الفقرات التي هي مراجعات إدراج.
// عيّن علامة "IgnoreInserted" إلى "false" للحصول على عملية البحث والاستبدال
// لتبحث أيضًا عن النص داخل مراجعات الإدراج.
options->set_IgnoreInserted(ignoreTextInsideInsertRevisions);

doc->get_Range()->Replace(u"Hello", u"Greetings", options);

ASSERT_EQ(ignoreTextInsideInsertRevisions ? System::String(u"Greetings world!\rHello again!") : System::String(u"Greetings world!\rGreetings again!"), doc->GetText().Trim());
```

## انظر أيضًا

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
