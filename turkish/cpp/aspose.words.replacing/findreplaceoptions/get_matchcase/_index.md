---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_MatchCase yöntemi"
linktitle: "get_MatchCase"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_MatchCase yöntemi. True, büyük/küçük harfe duyarlı karşılaştırmayı, false ise büyük/küçük harfe duyarsız karşılaştırmayı C++'de gösterir."
type: docs
weight: 14000
url: /tr/cpp/aspose.words.replacing/findreplaceoptions/get_matchcase/
---
## FindReplaceOptions::get_MatchCase method


True, büyük/küçük harfe duyarlı karşılaştırmayı; false, büyük/küçük harfe duyarsız karşılaştırmayı gösterir.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_MatchCase() const
```


## Örnekler



Bir bul-ve-değiştir işlemi sırasında büyük/küçük harf duyarlılığını nasıl değiştireceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Ruby bought a ruby necklace.");

// "FindReplaceOptions" nesnesini kullanarak bul-ve-değiştir sürecini değiştirebiliriz.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// "MatchCase" bayrağını "true" olarak ayarlayarak değiştirilmek üzere bulunan dizgelere büyük/küçük harf duyarlılığı uygularsınız.
// "MatchCase" bayrağını "false" olarak ayarlayarak değiştirilmek üzere metin ararken karakterin büyük/küçük harfini yoksayarsınız.
options->set_MatchCase(matchCase);

doc->get_Range()->Replace(u"Ruby", u"Jade", options);

ASSERT_EQ(matchCase ? System::String(u"Jade bought a ruby necklace.") : System::String(u"Jade bought a Jade necklace."), doc->GetText().Trim());
```

## Ayrıca Bakınız

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
