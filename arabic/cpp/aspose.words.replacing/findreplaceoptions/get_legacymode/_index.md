---
title: "طريقة Aspose::Words::Replacing::FindReplaceOptions::get_LegacyMode"
linktitle: "get_LegacyMode"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Replacing::FindReplaceOptions::get_LegacyMode. تحصل أو تضبط قيمة منطقية تشير إلى أن خوارزمية البحث/الاستبدال القديمة تُستخدم في C++."
type: docs
weight: 13000
url: /ar/cpp/aspose.words.replacing/findreplaceoptions/get_legacymode/
---
## FindReplaceOptions::get_LegacyMode method


يحصل أو يعيّن قيمة منطقية تشير إلى أن خوارزمية البحث/الاستبدال القديمة تُستخدم.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_LegacyMode() const
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

## انظر أيضًا

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
