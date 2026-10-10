---
title: "طريقة Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFieldCodes"
linktitle: "get_IgnoreFieldCodes"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFieldCodes. يحصل على أو يضبط قيمة منطقية تشير إلى ما إذا كان يجب تجاهل النص داخل رموز الحقول. القيمة الافتراضية هي false في C++."
type: docs
weight: 8000
url: /ar/cpp/aspose.words.replacing/findreplaceoptions/get_ignorefieldcodes/
---
## FindReplaceOptions::get_IgnoreFieldCodes method


يحصل أو يعيّن قيمة منطقية تشير إلى ما إذا كان يجب تجاهل النص داخل رموز الحقول. القيمة الافتراضية هي **false**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFieldCodes() const
```

## ملاحظات


هذا الخيار يؤثر فقط على رموز الحقول (لا يتجاهل العقد بين [FieldSeparator](../../../aspose.words/nodetype/) و[FieldEnd](../../../aspose.words/nodetype/)).

لتجاهل الحقل بالكامل، يرجى استخدام الخيار المقابل [IgnoreFields](../get_ignorefields/).

## أمثلة



يوضح كيفية تجاهل النص داخل رموز الحقول.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertField(u"INCLUDETEXT", u"Test IT!");

auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
options->set_IgnoreFieldCodes(ignoreFieldCodes);

// استبدل 'T' في المستند مع تجاهل النص داخل رمز الحقل أو لا.
doc->get_Range()->Replace(System::MakeObject<System::Text::RegularExpressions::Regex>(u"T"), u"*", options);
std::cout << doc->GetText() << std::endl;

ASSERT_EQ(ignoreFieldCodes ? System::String(u"\u0013INCLUDETEXT\u0014*est I*!\u0015") : System::String(u"\u0013INCLUDE*EX*\u0014*est I*!\u0015"), doc->GetText().Trim());
```

## انظر أيضًا

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
