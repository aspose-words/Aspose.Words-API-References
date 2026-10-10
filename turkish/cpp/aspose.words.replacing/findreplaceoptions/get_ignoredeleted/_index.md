---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreDeleted metodu"
linktitle: "get_IgnoreDeleted"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreDeleted metodu. Silme revizyonları içindeki metni yok sayıp saymayacağını belirten bir boolean değerini alır veya ayarlar. Varsayılan değer C++'da false'tur."
type: docs
weight: 7000
url: /tr/cpp/aspose.words.replacing/findreplaceoptions/get_ignoredeleted/
---
## FindReplaceOptions::get_IgnoreDeleted method


Silme revizyonları içindeki metni yoksaymayı belirten bir boolean değeri alır veya ayarlar. Varsayılan değer **false**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreDeleted() const
```


## Örnekler



Bir bul-ve-değiştir işlemi sırasında silme revizyonları içindeki metni dahil etmeyi veya yok saymayı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");
builder->Writeln(u"Hello again!");

// Revizyon takibini başlatın ve ikinci paragrafı kaldırın, bu bir silme revizyonu oluşturacaktır.
// Bu paragraf, silme revizyonunu kabul edene kadar belgede kalacaktır.
doc->StartTrackRevisions(u"John Doe", System::DateTime::get_Now());
doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(1)->Remove();
doc->StopTrackRevisions();

ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(1)->get_IsDeleteRevision());

// Bul ve değiştir sürecini değiştirmek için bir \"FindReplaceOptions\" nesnesi kullanabiliriz.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// Bul ve değiştir işlemini elde etmek için \"IgnoreDeleted\" bayrağını \"true\" olarak ayarlayın
// işlemi, silme revizyonu olan paragrafları yok sayacak şekilde.
// Bul ve değiştir işlemini elde etmek için \"IgnoreDeleted\" bayrağını \"false\" olarak ayarlayın
// işlemi, silme revizyonları içindeki metni de arayacak şekilde.
options->set_IgnoreDeleted(ignoreTextInsideDeleteRevisions);

doc->get_Range()->Replace(u"Hello", u"Greetings", options);

ASSERT_EQ(ignoreTextInsideDeleteRevisions ? System::String(u"Greetings world!\rHello again!") : System::String(u"Greetings world!\rGreetings again!"), doc->GetText().Trim());
```

## Ayrıca Bakınız

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
