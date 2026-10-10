---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_SmartParagraphBreakReplacement metodu"
linktitle: "get_SmartParagraphBreakReplacement"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_SmartParagraphBreakReplacement metodu. Sonraki kardeş paragraf bulunmadığında paragraf sonu karakterinin değiştirilmesine izin verilip verilmeyeceğini belirten bir boolean değer alır veya ayarlar. Varsayılan değer C++'da false."
type: docs
weight: 16000
url: /tr/cpp/aspose.words.replacing/findreplaceoptions/get_smartparagraphbreakreplacement/
---
## FindReplaceOptions::get_SmartParagraphBreakReplacement method


Paragraf kırılımının, sonraki kardeş paragraf yoksa değiştirilmesine izin verilip verilmediğini gösteren bir boolean değerini alır veya ayarlar. Varsayılan değer **false**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_SmartParagraphBreakReplacement() const
```


## Örnekler



İç içe bir tablo içeren bir tablo hücresinden paragrafın nasıl kaldırılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// İlk hücrede paragraf ve iç tablo içeren bir tablo oluşturun.
builder->StartTable();
builder->InsertCell();
builder->Write(u"TEXT1");
builder->StartTable();
builder->InsertCell();
builder->EndTable();
builder->EndTable();
builder->Writeln();

auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
// Aşağıdaki seçenek 'true' olarak ayarlandığında, Aspose.Words paragrafın metnini kaldıracaktır
// tamamen paragraf işaretiyle birlikte. Aksi takdirde, Aspose.Words Word'ü taklit ederek kaldıracaktır
// sadece paragrafın metnini ve paragraf işaretini olduğu gibi bırakır (metni bir tablo izlediğinde).
options->set_SmartParagraphBreakReplacement(isSmartParagraphBreakReplacement);
doc->get_Range()->Replace(System::MakeObject<System::Text::RegularExpressions::Regex>(u"TEXT1&p"), u"", options);

doc->Save(get_ArtifactsDir() + u"Table.RemoveParagraphTextAndMark.docx");
```

## Ayrıca Bakınız

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
