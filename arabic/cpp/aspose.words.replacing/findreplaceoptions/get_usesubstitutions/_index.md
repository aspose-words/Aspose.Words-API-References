---
title: "طريقة Aspose::Words::Replacing::FindReplaceOptions::get_UseSubstitutions"
linktitle: "get_UseSubstitutions"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Replacing::FindReplaceOptions::get_UseSubstitutions. يحصل أو يضبط قيمة منطقية تشير إلى ما إذا كان يجب التعرف على الاستبدالات واستخدامها داخل أنماط الاستبدال. القيمة الافتراضية هي false في C++."
type: docs
weight: 18000
url: /ar/cpp/aspose.words.replacing/findreplaceoptions/get_usesubstitutions/
---
## FindReplaceOptions::get_UseSubstitutions method


يحصل أو يعيّن قيمة منطقية تشير إلى ما إذا كان يجب التعرف على الاستبدالات واستخدامها داخل أنماط الاستبدال. القيمة الافتراضية هي **false**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_UseSubstitutions() const
```


## أمثلة



يظهر كيفية التعرف على الاستبدالات واستخدامها داخل أنماط الاستبدال.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Jason gave money to Paul.");

auto regex = System::MakeObject<System::Text::RegularExpressions::Regex>(u"([A-z]+) gave money to ([A-z]+)");

auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
options->set_UseSubstitutions(true);

// استخدام وضع التوافق القديم لا يدعم العديد من الميزات المتقدمة، لذا نحتاج إلى ضبطه على 'false'.
options->set_LegacyMode(false);

doc->get_Range()->Replace(regex, u"$2 took money from $1", options);

ASSERT_EQ(doc->GetText(), u"Paul took money from Jason.\f");
```


يظهر كيفية استبدال النص بالاستبدالات.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"John sold a car to Paul.");
builder->Writeln(u"Jane sold a house to Joe.");

// يمكننا استخدام كائن "FindReplaceOptions" لتعديل عملية البحث والاستبدال.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// قم بتعيين الخاصية "UseSubstitutions" إلى "true" للحصول على
// عملية البحث والاستبدال للتعرف على عناصر الاستبدال.
// قم بتعيين الخاصية "UseSubstitutions" إلى "false" لتجاهل عناصر الاستبدال.
options->set_UseSubstitutions(useSubstitutions);

auto regex = System::MakeObject<System::Text::RegularExpressions::Regex>(u"([A-z]+) sold a ([A-z]+) to ([A-z]+)");
doc->get_Range()->Replace(regex, u"$3 bought a $2 from $1", options);

ASSERT_EQ(useSubstitutions ? System::String(u"Paul bought a car from John.\rJoe bought a house from Jane.") : System::String(u"$3 bought a $2 from $1.\r$3 bought a $2 from $1."), doc->GetText().Trim());
```

## انظر أيضًا

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
