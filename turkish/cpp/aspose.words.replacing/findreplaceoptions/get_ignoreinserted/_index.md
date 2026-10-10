---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreInserted yöntemi"
linktitle: "get_IgnoreInserted"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreInserted yöntemi. Ekleme revizyonları içindeki metni göz ardı edip etmeyeceğini belirten bir boolean değer alır veya ayarlar. Varsayılan değer C++'ta false'tur."
type: docs
weight: 11000
url: /tr/cpp/aspose.words.replacing/findreplaceoptions/get_ignoreinserted/
---
## FindReplaceOptions::get_IgnoreInserted method


Ekleme revizyonları içindeki metni yoksaymayı belirten bir boolean değeri alır veya ayarlar. Varsayılan değer **false**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreInserted() const
```


## Örnekler



Bir bul ve değiştir işlemi sırasında ekleme revizyonları içindeki metni dahil etme veya göz ardı etme yöntemini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");

// Revizyon takibini başlatın ve bir paragraf ekleyin. Bu paragraf bir ekleme revizyonu olacaktır.
doc->StartTrackRevisions(u"John Doe", System::DateTime::get_Now());
builder->Writeln(u"Hello again!");
doc->StopTrackRevisions();

ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(1)->get_IsInsertRevision());

// "FindReplaceOptions" nesnesini kullanarak bul-ve-değiştir sürecini değiştirebiliriz.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// "IgnoreInserted" bayrağını "true" olarak ayarlayarak bul ve değiştir
// işlemi, ekleme revizyonu olan paragrafları göz ardı edecek şekilde.
// "IgnoreInserted" bayrağını "false" olarak ayarlayarak bul ve değiştir
// işlemi, ekleme revizyonları içindeki metni de arayacak şekilde.
options->set_IgnoreInserted(ignoreTextInsideInsertRevisions);

doc->get_Range()->Replace(u"Hello", u"Greetings", options);

ASSERT_EQ(ignoreTextInsideInsertRevisions ? System::String(u"Greetings world!\rHello again!") : System::String(u"Greetings world!\rGreetings again!"), doc->GetText().Trim());
```

## Ayrıca Bakınız

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
