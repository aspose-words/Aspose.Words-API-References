---
title: "Aspose::Words::Hyphenation::RegisterDictionary metodu"
linktitle: "RegisterDictionary"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Hyphenation::RegisterDictionary metodu. Belirtilen dil için bir akıştan heceleme sözlüğü kaydeder ve yükler. Sözlük okunamıyorsa veya geçersiz biçimdeyse C++ içinde bir istisna fırlatır."
type: docs
weight: 4000
url: /tr/cpp/aspose.words/hyphenation/registerdictionary/
---
## Hyphenation::RegisterDictionary(const System::String\&, const System::SharedPtr\<System::IO::Stream\>\&) method


Belirtilen dil için bir akıştan heceleme sözlüğü kaydeder ve yükler. Sözlük okunamıyorsa veya geçersiz biçimdeyse istisna fırlatır.

```cpp
static void Aspose::Words::Hyphenation::RegisterDictionary(const System::String &language, const System::SharedPtr<System::IO::Stream> &stream)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| dil | const System::String\& | Bir dil adı, ör. "en-US". "culture name" için .NET belgelerine ve ayrıntılar için RFC 4646'ya bakın. |
| akış | const System::SharedPtr\<System::IO::Stream\>\& | OpenOffice biçimindeki sözlük dosyası için bir akış. |

## Ayrıca Bakınız

* Class [Hyphenation](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Hyphenation::RegisterDictionary(const System::String\&, const System::String\&) method


Belirtilen dil için dosyadan bir heceleme sözlüğü kaydeder ve yükler. Sözlük okunamıyorsa veya geçersiz biçimdeyse bir istisna fırlatır. Bu metod aynı zamanda aynı dil için [Callback](../get_callback/) tekrar tekrar çağrılmasını önlemek amacıyla Null sözlüğü kaydetmek için de kullanılabilir.

```cpp
static void Aspose::Words::Hyphenation::RegisterDictionary(const System::String &language, const System::String &fileName)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| dil | const System::String\& | Bir dil adı, ör. "en-US". "culture name" için .NET belgelerine ve ayrıntılar için RFC 4646'ya bakın. |
| fileName | const System::String\& | Open Office biçimindeki sözlük dosyasına bir yol. Bu parametre **null** veya boş bir dize ise, kaydedilen Null sözlük olur ve bu dil için callback artık çağrılmaz. Callback'i tekrar etkinleştirmek için [UnregisterDictionary()](../) metodunu kullanın. |

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
## Hyphenation::RegisterDictionary(System::String, std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> static void Aspose::Words::Hyphenation::RegisterDictionary(System::String language, std::basic_istream<CharType, Traits> &stream)
```

## Ayrıca Bakınız

* Class [Hyphenation](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
