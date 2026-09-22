---
title: "Aspose::Words::Range::Replace metodu"
linktitle: "Değiştir"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Range::Replace metodu. Bir düzenli ifadeyle belirtilen karakter deseninin tüm eşleşmelerini başka bir dizeyle C++'ta değiştirir."
type: docs
weight: 12000
url: /tr/cpp/aspose.words/range/replace/
---
## Range::Replace(const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) method


Düzenli ifade ile belirtilen karakter deseninin tüm görünümlerini başka bir dizeyle değiştirir.

```cpp
int32_t Aspose::Words::Range::Replace(const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| desen | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | Eşleşmeleri bulmak için kullanılan bir düzenli ifade deseni. |
| değiştirme | const System::String\& | Desenin tüm eşleşmelerini değiştirmek için bir dize. |

### ReturnValue

Yapılan değiştirme sayısı.
## Açıklamalar


Düzenli ifade tarafından yakalanan tüm eşleşmeyi değiştirir.

Metod, desen ve değiştirme dizelerindeki satır sonlarını işleyebilir.

Satır sonlarıyla çalışmanız gerekiyorsa özel meta karakterler kullanmalısınız:

* **%&p** - paragraph break
* **%&b** - section break
* **%&m** - page break
* **%&l** - manual line break



## Örnekler



Bir düzenli ifade kalıbının tüm tekrarlarını başka bir metinle nasıl değiştireceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"I decided to get the curtains in gray, ideal for the grey-accented room.");

doc->get_Range()->Replace(System::MakeObject<System::Text::RegularExpressions::Regex>(u"gr(a|e)y"), u"lavender");

ASSERT_EQ(u"I decided to get the curtains in lavender, ideal for the lavender-accented room.", doc->GetText().Trim());
```

## Ayrıca Bakınız

* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Range::Replace(const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


Düzenli ifade ile belirtilen karakter deseninin tüm görünümlerini başka bir dizeyle değiştirir.

```cpp
int32_t Aspose::Words::Range::Replace(const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| desen | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | Eşleşmeleri bulmak için kullanılan bir düzenli ifade deseni. |
| değiştirme | const System::String\& | Desenin tüm eşleşmelerini değiştirmek için bir dize. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) nesnesi ek seçenekleri belirtmek için. |

### ReturnValue

Yapılan değiştirme sayısı.
## Açıklamalar


Düzenli ifade tarafından yakalanan tüm eşleşmeyi değiştirir.

Metod, desen ve değiştirme dizelerindeki satır sonlarını işleyebilir.

Satır sonlarıyla çalışmanız gerekiyorsa özel meta karakterler kullanmalısınız:

* **%&p** - paragraph break
* **%&b** - section break
* **%&m** - page break
* **%&l** - manual line break
* **%&&** - & character



## Ayrıca Bakınız

* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Range::Replace(const System::String\&, const System::String\&) method


Belirtilen karakter dizesi deseninin tüm görünümlerini bir değiştirme dizesiyle değiştirir.

```cpp
int32_t Aspose::Words::Range::Replace(const System::String &pattern, const System::String &replacement)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| desen | const System::String\& | Değiştirilecek bir dize. |
| değiştirme | const System::String\& | Desenin tüm eşleşmelerini değiştirmek için bir dize. |

### ReturnValue

Yapılan değiştirme sayısı.
## Açıklamalar


Kalıp düzenli ifade olarak kullanılmayacaktır. Düzenli ifadelere ihtiyacınız varsa lütfen [Replace()](../) kullanın.

Büyük/küçük harfe duyarsız karşılaştırma kullanıldı.

Metod, desen ve değiştirme dizelerindeki satır sonlarını işleyebilir.

Satır sonlarıyla çalışmanız gerekiyorsa özel meta karakterler kullanmalısınız:

* **%&p** - paragraph break
* **%&b** - section break
* **%&m** - page break
* **%&l** - manual line break



## Örnekler



Bir belgenin içeriğinde bul ve değiştir metin işlemini nasıl gerçekleştireceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Greetings, _FullName_!");

// Belgemizin içeriğinde bir bul ve değiştir işlemi gerçekleştirip gerçekleşen değişiklik sayısını doğrulayın.
int32_t replacementCount = doc->get_Range()->Replace(u"_FullName_", u"John Doe");

ASSERT_EQ(1, replacementCount);
ASSERT_EQ(u"Greetings, John Doe!", doc->GetText().Trim());
```


Bir bul ve değiştir işleminin eşleşme bulduğu paragraflara biçim eklemenin nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Every paragraph that ends with a full stop like this one will be right aligned.");
builder->Writeln(u"This one will not!");
builder->Write(u"This one also will.");

System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

ASSERT_EQ(Aspose::Words::ParagraphAlignment::Left, paragraphs->idx_get(0)->get_ParagraphFormat()->get_Alignment());
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Left, paragraphs->idx_get(1)->get_ParagraphFormat()->get_Alignment());
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Left, paragraphs->idx_get(2)->get_ParagraphFormat()->get_Alignment());

// "FindReplaceOptions" nesnesini kullanarak bul-ve-değiştir sürecini değiştirebiliriz.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// "Alignment" özelliğini "ParagraphAlignment.Right" olarak ayarlayarak her paragrafı sağa hizalayın.
// bul ve değiştir işleminin bulduğu bir eşleşme içeren.
options->get_ApplyParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Right);

// Paragraf sonundan hemen önceki her nokta işaretini ünlem işaretiyle değiştirin.
int32_t count = doc->get_Range()->Replace(u".&p", u"!&p", options);

ASSERT_EQ(2, count);
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Right, paragraphs->idx_get(0)->get_ParagraphFormat()->get_Alignment());
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Left, paragraphs->idx_get(1)->get_ParagraphFormat()->get_Alignment());
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Right, paragraphs->idx_get(2)->get_ParagraphFormat()->get_Alignment());
ASSERT_EQ(System::String(u"Every paragraph that ends with a full stop like this one will be right aligned!\r") + u"This one will not!\r" + u"This one also will!", doc->GetText().Trim());
```

## Ayrıca Bakınız

* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Range::Replace(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


Belirtilen karakter dizesi deseninin tüm görünümlerini bir değiştirme dizesiyle değiştirir.

```cpp
int32_t Aspose::Words::Range::Replace(const System::String &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| desen | const System::String\& | Değiştirilecek bir dize. |
| değiştirme | const System::String\& | Desenin tüm eşleşmelerini değiştirmek için bir dize. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) nesnesi ek seçenekleri belirtmek için. |

### ReturnValue

Yapılan değiştirme sayısı.
## Açıklamalar


Kalıp düzenli ifade olarak kullanılmayacaktır. Düzenli ifadelere ihtiyacınız varsa lütfen [Replace()](../) kullanın.

Metod, desen ve değiştirme dizelerindeki satır sonlarını işleyebilir.

Satır sonlarıyla çalışmanız gerekiyorsa özel meta karakterler kullanmalısınız:

* **%&p** - paragraph break
* **%&b** - section break
* **%&m** - page break
* **%&l** - manual line break
* **%&&** - & character



## Örnekler



Bir belgenin altbilgisindeki metni nasıl değiştireceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Footer.docx");

System::SharedPtr<Aspose::Words::HeaderFooterCollection> headersFooters = doc->get_FirstSection()->get_HeadersFooters();
System::SharedPtr<Aspose::Words::HeaderFooter> footer = headersFooters->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary);

auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
options->set_MatchCase(false);
options->set_FindWholeWordsOnly(false);

int32_t currentYear = System::DateTime::get_Now().get_Year();
footer->get_Range()->Replace(u"(C) 2006 Aspose Pty Ltd.", System::String::Format(u"Copyright (C) {0} by Aspose Pty Ltd.", currentYear), options);

doc->Save(get_ArtifactsDir() + u"HeaderFooter.ReplaceText.docx");
```


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


Yalnızca bağımsız kelimeler için bul-ve-değiştir işlemlerini nasıl değiştireceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Jackson will meet you in Jacksonville.");

// "FindReplaceOptions" nesnesini kullanarak bul-ve-değiştir sürecini değiştirebiliriz.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// "FindWholeWordsOnly" bayrağını "true" olarak ayarlayarak bulunan metin başka bir kelimenin parçası değilse değiştirirsiniz.
// "FindWholeWordsOnly" bayrağını "false" olarak ayarlayarak çevresine bakılmaksızın tüm metni değiştirirsiniz.
options->set_FindWholeWordsOnly(findWholeWordsOnly);

doc->get_Range()->Replace(u"Jackson", u"Louis", options);

ASSERT_EQ(findWholeWordsOnly ? System::String(u"Louis will meet you in Jacksonville.") : System::String(u"Louis will meet you in Louisville."), doc->GetText().Trim());
```


Bir tablo ve hücredeki metin dizesinin tüm örneklerini nasıl değiştireceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Carrots");
builder->InsertCell();
builder->Write(u"50");
builder->EndRow();
builder->InsertCell();
builder->Write(u"Potatoes");
builder->InsertCell();
builder->Write(u"50");
builder->EndTable();

auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
options->set_MatchCase(true);
options->set_FindWholeWordsOnly(true);

// Tüm bir tablo üzerinde bul ve değiştir işlemi yapın.
table->get_Range()->Replace(u"Carrots", u"Eggs", options);

// Tablonun son satırının son hücresinde bul ve değiştir işlemi gerçekleştirin.
table->get_LastRow()->get_LastCell()->get_Range()->Replace(u"50", u"20", options);

ASSERT_EQ(System::String(u"Eggs\a50\a\a") + u"Potatoes\a20\a\a", table->GetText().Trim());
```

## Ayrıca Bakınız

* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
