---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFields metodu"
linktitle: "get_IgnoreFields"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFields metodu. Alanlar içindeki metni yok sayıp saymayacağını belirten bir boolean değerini alır veya ayarlar. Varsayılan değer C++'da false'tur."
type: docs
weight: 9000
url: /tr/cpp/aspose.words.replacing/findreplaceoptions/get_ignorefields/
---
## FindReplaceOptions::get_IgnoreFields method


Alanlar içindeki metni yoksaymayı belirten bir boolean değeri alır veya ayarlar. Varsayılan değer **false**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFields() const
```

## Açıklamalar


Bu seçenek tüm alanı etkiler (tüm düğümler [FieldStart](../../../aspose.words/nodetype/) ve [FieldEnd](../../../aspose.words/nodetype/) arasında).

Yalnızca alan kodlarını yok saymak için lütfen ilgili seçenek olan [IgnoreFieldCodes](../get_ignorefieldcodes/) kullanın.

## Örnekler



Alanlar içindeki metni yok saymayı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");
builder->InsertField(u"QUOTE", u"Hello again!");

// "FindReplaceOptions" nesnesini kullanarak bul-ve-değiştir sürecini değiştirebiliriz.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// Bul ve değiştir işlemini elde etmek için \"IgnoreFields\" bayrağını \"true\" olarak ayarlayın
// işlemi, alanlar içindeki metni yok sayacak şekilde.
// Bul ve değiştir işlemini elde etmek için \"IgnoreFields\" bayrağını \"false\" olarak ayarlayın
// işlemi, alanlar içindeki metni de arayacak şekilde.
options->set_IgnoreFields(ignoreTextInsideFields);

doc->get_Range()->Replace(u"Hello", u"Greetings", options);

ASSERT_EQ(ignoreTextInsideFields ? System::String(u"Greetings world!\r\u0013QUOTE\u0014Hello again!\u0015") : System::String(u"Greetings world!\r\u0013QUOTE\u0014Greetings again!\u0015"), doc->GetText().Trim());
```

## Ayrıca Bakınız

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
