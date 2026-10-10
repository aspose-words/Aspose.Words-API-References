---
title: "Aspose::Words::Hyphenation::IsDictionaryRegistered yöntemi"
linktitle: "IsDictionaryRegistered"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Hyphenation::IsDictionaryRegistered yöntemi. Belirtilen dil için kayıtlı bir sözlük yoksa veya kayıtlı sözlük Null ise false, aksi takdirde true döndürür C++'ta."
type: docs
weight: 3000
url: /tr/cpp/aspose.words/hyphenation/isdictionaryregistered/
---
## Hyphenation::IsDictionaryRegistered method


Belirtilen dil için kayıtlı sözlük yoksa veya kayıtlı sözlük Null ise **false**, aksi takdirde **true** döndürür.

```cpp
static bool Aspose::Words::Hyphenation::IsDictionaryRegistered(const System::String &language)
```


## Örnekler



Bir hyphenation sözlüğünün nasıl kaydedileceğini gösterir.
```cpp
// Bir hyphenation sözlüğü, sözlüğün diline ait hyphenation kurallarını tanımlayan bir dizi karakter içerir.
// Bir belge, bir kelimenin bölünebilir ve bir sonraki satıra devam edebilir olduğu metin satırları içerdiğinde,
// hyphenation, o kelimenin alt dizelerini bulmak için sözlüğün karakter listesine bakar.
// Sözlük bir alt dize içeriyorsa, hyphenation kelimeyi iki satıra bölecektir
// alt dizeye göre ve ilk yarısına bir tire ekleyerek.
// Yerel dosya sisteminden bir sözlük dosyasını "de-CH" yerel ayarına kaydedin.
Aspose::Words::Hyphenation::RegisterDictionary(u"de-CH", get_MyDir() + u"hyph_de_CH.dic");

ASSERT_TRUE(Aspose::Words::Hyphenation::IsDictionaryRegistered(u"de-CH"));

// Sözlüğümüzle aynı yerel ayara sahip metin içeren bir belge açın,
// ve sabit sayfa kaydetme formatında kaydedin. O belgedeki metin hyphenation uygulanacaktır.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"German text.docx");

ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->LINQ_OfType<System::SharedPtr<Aspose::Words::Run> >()->LINQ_All(static_cast<System::Func<System::SharedPtr<Aspose::Words::Run>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Run> r)>>([](System::SharedPtr<Aspose::Words::Run> r) -> bool
{
    return r->get_Font()->get_LocaleId() == System::MakeObject<System::Globalization::CultureInfo>(u"de-CH")->get_LCID();
}))));

doc->Save(get_ArtifactsDir() + u"Hyphenation.Dictionary.Registered.pdf");

// Sözlüğün kaydını kaldırdıktan sonra belgeyi yeniden yükleyin,
// ve başka bir PDF olarak kaydedin; bu PDF'de hyphenation uygulanmış metin olmayacaktır.
Aspose::Words::Hyphenation::UnregisterDictionary(u"de-CH");

ASSERT_FALSE(Aspose::Words::Hyphenation::IsDictionaryRegistered(u"de-CH"));

doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"German text.docx");
doc->Save(get_ArtifactsDir() + u"Hyphenation.Dictionary.Unregistered.pdf");
```

## Ayrıca Bakınız

* Class [Hyphenation](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
