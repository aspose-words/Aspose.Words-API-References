---
title: "طريقة Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFields"
linktitle: "get_IgnoreFields"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFields. يحصل أو يضبط قيمة منطقية تشير إلى ما إذا كان يجب تجاهل النص داخل الحقول. القيمة الافتراضية هي false في C++."
type: docs
weight: 9000
url: /ar/cpp/aspose.words.replacing/findreplaceoptions/get_ignorefields/
---
## FindReplaceOptions::get_IgnoreFields method


يحصل أو يعيّن قيمة منطقية تشير إلى ما إذا كان يجب تجاهل النص داخل الحقول. القيمة الافتراضية هي **false**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFields() const
```

## ملاحظات


هذا الخيار يؤثر على الحقل بالكامل (جميع العقد بين [FieldStart](../../../aspose.words/nodetype/) و [FieldEnd](../../../aspose.words/nodetype/)).

لتجاهل رموز الحقول فقط، يرجى استخدام الخيار المقابل [IgnoreFieldCodes](../get_ignorefieldcodes/).

## أمثلة



يظهر كيفية تجاهل النص داخل الحقول.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");
builder->InsertField(u"QUOTE", u"Hello again!");

// يمكننا استخدام كائن "FindReplaceOptions" لتعديل عملية البحث والاستبدال.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// قم بتعيين علامة "IgnoreFields" إلى "true" للحصول على عملية البحث والاستبدال
// لتجاهل النص داخل الحقول.
// قم بتعيين علامة "IgnoreFields" إلى "false" للحصول على عملية البحث والاستبدال
// للبحث أيضًا عن النص داخل الحقول.
options->set_IgnoreFields(ignoreTextInsideFields);

doc->get_Range()->Replace(u"Hello", u"Greetings", options);

ASSERT_EQ(ignoreTextInsideFields ? System::String(u"Greetings world!\r\u0013QUOTE\u0014Hello again!\u0015") : System::String(u"Greetings world!\r\u0013QUOTE\u0014Greetings again!\u0015"), doc->GetText().Trim());
```

## انظر أيضًا

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
