---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFieldCodes metodu"
linktitle: "get_IgnoreFieldCodes"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFieldCodes metodu. Alan kodları içindeki metnin yok sayılıp sayılmayacağını belirten bir boolean değer alır veya ayarlar. Varsayılan değer C++'da false."
type: docs
weight: 8000
url: /tr/cpp/aspose.words.replacing/findreplaceoptions/get_ignorefieldcodes/
---
## FindReplaceOptions::get_IgnoreFieldCodes method


Alan kodları içindeki metni yoksaymayı belirten bir boolean değeri alır veya ayarlar. Varsayılan değer **false**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFieldCodes() const
```

## Açıklamalar


Bu seçenek yalnızca alan kodlarını etkiler ( [FieldSeparator](../../../aspose.words/nodetype/) ve [FieldEnd](../../../aspose.words/nodetype/) arasındaki düğümleri yok saymaz).

Tüm alanı yok saymak için lütfen ilgili seçenek olan [IgnoreFields](../get_ignorefields/) kullanın.

## Örnekler



Alan kodları içindeki metnin nasıl yok sayılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertField(u"INCLUDETEXT", u"Test IT!");

auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
options->set_IgnoreFieldCodes(ignoreFieldCodes);

// Belgedeki 'T' karakterini alan kodu içindeki metni göz ardı ederek değiştirin veya etmeyin.
doc->get_Range()->Replace(System::MakeObject<System::Text::RegularExpressions::Regex>(u"T"), u"*", options);
std::cout << doc->GetText() << std::endl;

ASSERT_EQ(ignoreFieldCodes ? System::String(u"\u0013INCLUDETEXT\u0014*est I*!\u0015") : System::String(u"\u0013INCLUDE*EX*\u0014*est I*!\u0015"), doc->GetText().Trim());
```

## Ayrıca Bakınız

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
