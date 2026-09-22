---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_LegacyMode yöntemi"
linktitle: "get_LegacyMode"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_LegacyMode yöntemi. C++'ta eski bul/değiştir algoritmasının kullanıldığını gösteren bir boolean değeri alır veya ayarlar."
type: docs
weight: 13000
url: /tr/cpp/aspose.words.replacing/findreplaceoptions/get_legacymode/
---
## FindReplaceOptions::get_LegacyMode method


Eski bul/değiştir algoritmasının kullanıldığını belirten bir boolean değeri alır veya ayarlar.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_LegacyMode() const
```


## Örnekler



Değiştirme kalıpları içinde yer tutucuları tanıma ve kullanma yöntemini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Jason gave money to Paul.");

auto regex = System::MakeObject<System::Text::RegularExpressions::Regex>(u"([A-z]+) gave money to ([A-z]+)");

auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
options->set_UseSubstitutions(true);

// Eski modun kullanılması birçok gelişmiş özelliği desteklemez, bu yüzden onu 'false' olarak ayarlamamız gerekir.
options->set_LegacyMode(false);

doc->get_Range()->Replace(regex, u"$2 took money from $1", options);

ASSERT_EQ(doc->GetText(), u"Paul took money from Jason.\f");
```

## Ayrıca Bakınız

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
