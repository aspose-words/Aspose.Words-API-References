---
title: "طريقة Aspose::Words::Replacing::FindReplaceOptions::get_MatchCase"
linktitle: "get_MatchCase"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Replacing::FindReplaceOptions::get_MatchCase. True تشير إلى مقارنة حساسة لحالة الأحرف، false تشير إلى مقارنة غير حساسة لحالة الأحرف في C++."
type: docs
weight: 14000
url: /ar/cpp/aspose.words.replacing/findreplaceoptions/get_matchcase/
---
## FindReplaceOptions::get_MatchCase method


True يدل على مقارنة حساسة لحالة الأحرف، false يدل على مقارنة غير حساسة لحالة الأحرف.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_MatchCase() const
```


## أمثلة



يوضح كيفية تبديل حساسية حالة الأحرف عند تنفيذ عملية البحث والاستبدال.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Ruby bought a ruby necklace.");

// يمكننا استخدام كائن "FindReplaceOptions" لتعديل عملية البحث والاستبدال.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// عيّن علم "MatchCase" إلى "true" لتطبيق حساسية حالة الأحرف أثناء البحث عن السلاسل لاستبدالها.
// عيّن علم "MatchCase" إلى "false" لتجاهل حالة الأحرف أثناء البحث عن النص لاستبداله.
options->set_MatchCase(matchCase);

doc->get_Range()->Replace(u"Ruby", u"Jade", options);

ASSERT_EQ(matchCase ? System::String(u"Jade bought a ruby necklace.") : System::String(u"Jade bought a Jade necklace."), doc->GetText().Trim());
```

## انظر أيضًا

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
