---
title: "Aspose::Words::NumberStyle enum"
linktitle: "NumberStyle"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::NumberStyle enum. C++'da bir liste, dipnot ve sonnot, sayfa numaraları için sayı stilini belirtir."
type: docs
weight: 103000
url: /tr/cpp/aspose.words/numberstyle/
---
## NumberStyle enum


Bir liste, dipnot ve sonnot, sayfa numaraları için sayı stilini belirtir.

```cpp
enum class NumberStyle
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| Arapça | 0 | Arapça numaralandırma (1, 2, 3, ...) |
| UppercaseRoman | 1 | Büyük harf Roman (I, II, III, ...) |
| LowercaseRoman | 2 | Küçük harf Roman (i, ii, iii, ...) |
| UppercaseLetter | 3 | Büyük harf (A, B, C, ...) |
| LowercaseLetter | 4 | Küçük harf (a, b, c, ...) |
| Ordinal | 5 | Ordinal (1., 2., 3., ...) |
| Number | 6 | Numbered (Bir, İki, Üç, ...) |
| OrdinalText | 7 | Ordinal (metin) (Birinci, İkinci, Üçüncü, ...) |
| Hex | 8 | Onaltılık: 8, 9, A, B, C, D, E, F, 10, 11, 12. |
| ChicagoManual | 9 | Chicago Kılavuzu [Stil](../style/): *, †, † |
| Kanji | 10 | İdeografik-dijital. |
| KanjiDigit | 11 | Japon sayımı. |
| AiueoHalfWidth | 12 | Aiueo. |
| IrohaHalfWidth | 13 | Iroha. |
| ArabicFullWidth | 14 | Tam genişlik Arapça: 1, 2, 3, 4. |
| ArabicHalfWidth | 15 | Yarı genişlik Arapça: 1, 2, 3, 4. |
| KanjiTraditional | 16 | Japon hukuki. |
| KanjiTraditional2 | 17 | Japon dijital on bin. |
| NumberInCircle | 18 | Kapsanmış daireler. |
| DecimalFullWidth | 19 | Ondalık tam genişlik: 1, 2, 3, 4. |
| Aiueo | 20 | Aiueo tam genişlik. |
| Iroha | 21 | Iroha tam genişlik. |
| LeadingZero | 22 | Ön Sıfır (01, 02,..., 09, 10, 11,..., 99, 100, 101,...) |
| Bullet | 23 | Madde işareti (metindeki karakter kodunu kontrol edin) |
| Ganada | 24 | Kore Ganada. |
| Chosung | 25 | Kore Chosung. |
| GB1 | 26 | Kapalı nokta. |
| GB2 | 27 | Kapalı parantez. |
| GB3 | 28 | Kapalı daire Çin. |
| GB4 | 29 | İdeograf kapalı daire. |
| Zodiac1 | 30 | İdeograf geleneksel. |
| Zodiac2 | 31 | İdeograf Zodyak. |
| Zodiac3 | 32 | İdeograf Zodyak geleneksel. |
| TradChinNum1 | 33 | Tayvan sayımı. |
| TradChinNum2 | 34 | İdeografik yasal geleneksel. |
| TradChinNum3 | 35 | Tayvan sayımı bin. |
| TradChinNum4 | 36 | Tayvan dijital. |
| SimpChinNum1 | 37 | Çince sayım. |
| SimpChinNum2 | 38 | Çince yasal sade. |
| SimpChinNum3 | 39 | Çince sayım bin. |
| SimpChinNum4 | 40 | Çince (uygulanmadı) |
| HanjaRead | 41 | Kore dijital. |
| HanjaReadDigit | 42 | Kore sayımı. |
| Hangul | 43 | Kore hukuku. |
| Hanja | 44 | Kore dijital2. |
| Hebrew1 | 45 | Hebrew-1. |
| Arabic1 | 46 | Arap alfası. |
| Hebrew2 | 47 | Hebrew-2. |
| Arabic2 | 48 | Arap abjadı. |
| HindiLetter1 | 49 | Hint sesli harfleri. |
| HindiLetter2 | 50 | Hintçe ünsüzler. |
| HindiArabic | 51 | Hintçe sayılar. |
| HindiCardinalText | 52 | Hintçe tanımlayıcı (kardinal) |
| ThaiLetter | 53 | Thai harfleri. |
| ThaiArabic | 54 | Thai sayıları. |
| ThaiCardinalText | 55 | Thai tanımlayıcı (kardinal) |
| VietCardinalText | 56 | Vietnamca tanımlayıcı (kardinal) |
| NumberInDash | 57 | Sayfa numarası biçimi: - 1 -, - 2 -, - 3 -, - 4 -. |
| LowercaseRussian | 58 | Küçük harfli Rus alfabesi. |
| BüyükHarflıRusça | 59 | Büyük harfli Rus alfabesi. |
| None | 255 | Madde işareti veya numara yok. |
| Özel | 65280 | Özel sayı biçimi. Yalnızca DOCX formatı tarafından desteklenir. |


## Örnekler



Özel liste biçimlendirmesini paragraflara uygulamanın nasıl yapılacağını, [DocumentBuilder](../documentbuilder/) kullanırken gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Bir liste, paragraf gruplarını ön ek sembolleri ve girintilerle düzenlememizi ve süslememizi sağlar.
// Girintiyi artırarak iç içe listeler oluşturabiliriz.
// Bir belge oluşturucunun "ListFormat" özelliğini kullanarak bir listeyi başlatabilir ve sonlandırabiliriz.
// Bir listenin başlangıcı ile sonu arasına eklediğimiz her paragraf, listenin bir öğesi haline gelir.
// Microsoft Word şablonundan bir liste oluşturun ve liste seviyelerinin ilk ikisini özelleştirin.
System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault);

System::SharedPtr<Aspose::Words::Lists::ListLevel> listLevel = list->get_ListLevels()->idx_get(0);
listLevel->get_Font()->set_Color(System::Drawing::Color::get_Red());
listLevel->get_Font()->set_Size(24);
listLevel->set_NumberStyle(Aspose::Words::NumberStyle::OrdinalText);
listLevel->set_StartAt(21);
listLevel->set_NumberFormat(u"\x0000");

listLevel->set_NumberPosition(-36);
listLevel->set_TextPosition(144);
listLevel->set_TabPosition(144);

listLevel = list->get_ListLevels()->idx_get(1);
listLevel->set_Alignment(Aspose::Words::Lists::ListLevelAlignment::Right);
listLevel->set_NumberStyle(Aspose::Words::NumberStyle::Bullet);
listLevel->get_Font()->set_Name(u"Wingdings");
listLevel->get_Font()->set_Color(System::Drawing::Color::get_Blue());
listLevel->get_Font()->set_Size(24);

// Bu NumberFormat değeri yıldız şeklinde madde işareti listesi sembolleri oluşturur.
listLevel->set_NumberFormat(u"\xf0af");
listLevel->set_TrailingCharacter(Aspose::Words::Lists::ListTrailingCharacter::Space);
listLevel->set_NumberPosition(144);

// Paragraflar oluşturun ve özel liste biçimlendirmemizin iki liste seviyesini onlara uygulayın.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_ListFormat()->set_List(list);
builder->Writeln(u"The quick brown fox...");
builder->Writeln(u"The quick brown fox...");

builder->get_ListFormat()->ListIndent();
builder->Writeln(u"jumped over the lazy dog.");
builder->Writeln(u"jumped over the lazy dog.");

builder->get_ListFormat()->ListOutdent();
builder->Writeln(u"The quick brown fox...");

builder->get_ListFormat()->RemoveNumbers();

builder->get_Document()->Save(get_ArtifactsDir() + u"Lists.CreateCustomList.docx");
```

## Ayrıca Bakınız

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
