---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_UseSubstitutions metodu"
linktitle: "get_UseSubstitutions"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_UseSubstitutions metodu. Değiştirme kalıpları içinde ikameleri tanıyıp kullanıp kullanmayacağını belirten bir boolean değerini alır veya ayarlar. Varsayılan değer C++'da false'tur."
type: docs
weight: 18000
url: /tr/cpp/aspose.words.replacing/findreplaceoptions/get_usesubstitutions/
---
## FindReplaceOptions::get_UseSubstitutions method


Değiştirme kalıpları içinde ikameleri tanıma ve kullanma durumunu gösteren bir boolean değerini alır veya ayarlar. Varsayılan değer **false**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_UseSubstitutions() const
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


Metni yer tutucularla nasıl değiştireceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"John sold a car to Paul.");
builder->Writeln(u"Jane sold a house to Joe.");

// "FindReplaceOptions" nesnesini kullanarak bul-ve-değiştir sürecini değiştirebiliriz.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// "UseSubstitutions" özelliğini "true" olarak ayarlayın
// bul ve değiştir işleminin yer tutucu öğeleri tanıması için.
// "UseSubstitutions" özelliğini "false" olarak ayarlayın ve yer tutucu öğeleri yok sayın.
options->set_UseSubstitutions(useSubstitutions);

auto regex = System::MakeObject<System::Text::RegularExpressions::Regex>(u"([A-z]+) sold a ([A-z]+) to ([A-z]+)");
doc->get_Range()->Replace(regex, u"$3 bought a $2 from $1", options);

ASSERT_EQ(useSubstitutions ? System::String(u"Paul bought a car from John.\rJoe bought a house from Jane.") : System::String(u"$3 bought a $2 from $1.\r$3 bought a $2 from $1."), doc->GetText().Trim());
```

## Ayrıca Bakınız

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
