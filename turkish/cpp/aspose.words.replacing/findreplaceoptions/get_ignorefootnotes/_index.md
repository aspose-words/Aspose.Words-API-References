---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFootnotes metodu"
linktitle: "get_IgnoreFootnotes"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFootnotes metodu. Altbilgileri yok sayıp saymayacağını belirten bir boolean değerini alır veya ayarlar. Varsayılan değer C++'da false'tur."
type: docs
weight: 10000
url: /tr/cpp/aspose.words.replacing/findreplaceoptions/get_ignorefootnotes/
---
## FindReplaceOptions::get_IgnoreFootnotes method


Dipnotları yoksaymayı belirten bir boolean değeri alır veya ayarlar. Varsayılan değer **false**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFootnotes() const
```


## Örnekler



Bir bul-ve-değiştir işlemi sırasında altbilgileri nasıl yok sayacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

builder->InsertParagraph();

builder->Write(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

// "IgnoreFootnotes" bayrağını "true" olarak ayarlayın bul-ve-değiştir işlemini elde etmek için
// işlemi, altbilgiler içindeki metni yok saymak için.
// "IgnoreFootnotes" bayrağını "false" olarak ayarlayın bul-ve-değiştir işlemini elde etmek için
// işlemi, aynı zamanda altbilgiler içindeki metni aramak için.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
options->set_IgnoreFootnotes(isIgnoreFootnotes);
doc->get_Range()->Replace(u"Lorem ipsum", u"Replaced Lorem ipsum", options);
```

## Ayrıca Bakınız

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
