---
title: "Aspose::Words::Replacing::FindReplaceOptions sınıfı"
linktitle: "FindReplaceOptions"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Replacing::FindReplaceOptions sınıfı. Bul/Değiştir işlemleri için seçenekleri belirtir. Daha fazla bilgi için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 1000
url: /tr/cpp/aspose.words.replacing/findreplaceoptions/
---
## FindReplaceOptions class


Bul/değiştir işlemleri için seçenekleri belirtir. Daha fazla bilgi için, [Find and Replace](https://docs.aspose.com/words/cpp/find-and-replace/) dokümantasyon makalesini ziyaret edin.

```cpp
class FindReplaceOptions : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [FindReplaceOptions](./findreplaceoptions/)() | Yeni bir [FindReplaceOptions](./) sınıfının örneğini varsayılan ayarlarla başlatır. |
| [FindReplaceOptions](./findreplaceoptions/)(Aspose::Words::Replacing::FindReplaceDirection) | Belirtilen yön ile yeni bir [FindReplaceOptions](./) sınıfının örneğini başlatır. |
| [FindReplaceOptions](./findreplaceoptions/)(const System::SharedPtr\<Aspose::Words::Replacing::IReplacingCallback\>\&) | Belirtilen değiştirme geri çağrısı ile yeni bir [FindReplaceOptions](./) sınıfının örneğini başlatır. |
| [FindReplaceOptions](./findreplaceoptions/)(Aspose::Words::Replacing::FindReplaceDirection, const System::SharedPtr\<Aspose::Words::Replacing::IReplacingCallback\>\&) | Belirtilen yön ve değiştirme geri çağrısı ile yeni bir [FindReplaceOptions](./) sınıfının örneğini başlatır. |
| [get_ApplyFont](./get_applyfont/)() const | Yeni içeriğe uygulanan metin biçimlendirmesi. |
| [get_ApplyParagraphFormat](./get_applyparagraphformat/)() const | Yeni içeriğe uygulanan [Paragraph](../../aspose.words/paragraph/) biçimlendirmesi. |
| [get_Direction](./get_direction/)() const | Değiştirme yönünü seçer. Varsayılan değer [Forward](../findreplacedirection/). |
| [get_FindWholeWordsOnly](./get_findwholewordsonly/)() const | True, oldValue'nun bağımsız bir kelime olması gerektiğini gösterir. |
| [get_IgnoreDeleted](./get_ignoredeleted/)() const | Silme revizyonları içindeki metni yoksaymayı belirten bir boolean değeri alır veya ayarlar. Varsayılan değer **false**. |
| [get_IgnoreFieldCodes](./get_ignorefieldcodes/)() const | Alan kodları içindeki metni yoksaymayı belirten bir boolean değeri alır veya ayarlar. Varsayılan değer **false**. |
| [get_IgnoreFields](./get_ignorefields/)() const | Alanlar içindeki metni yoksaymayı belirten bir boolean değeri alır veya ayarlar. Varsayılan değer **false**. |
| [get_IgnoreFootnotes](./get_ignorefootnotes/)() const | Dipnotları yoksaymayı belirten bir boolean değeri alır veya ayarlar. Varsayılan değer **false**. |
| [get_IgnoreInserted](./get_ignoreinserted/)() const | Ekleme revizyonları içindeki metni yoksaymayı belirten bir boolean değeri alır veya ayarlar. Varsayılan değer **false**. |
| [get_IgnoreOfficeMath](./get_ignoreofficemath/)() const | OfficeMath/> içindeki metni yoksaymayı belirten bir boolean değeri alır veya ayarlar. Varsayılan değer **true**. |
| [get_IgnoreShapes](./get_ignoreshapes/)() const | Metin içindeki şekilleri yoksaymayı belirten bir boolean değeri alır veya ayarlar. Varsayılan değer **false**. |
| [get_IgnoreStructuredDocumentTags](./get_ignorestructureddocumenttags/)() const | [StructuredDocumentTag](../../aspose.words.markup/structureddocumenttag/) içeriğini yoksaymayı belirten bir boolean değeri alır veya ayarlar. Varsayılan değer **false**. |
| [get_LegacyMode](./get_legacymode/)() const | Eski bul/değiştir algoritmasının kullanıldığını belirten bir boolean değeri alır veya ayarlar. |
| [get_MatchCase](./get_matchcase/)() const | True, büyük/küçük harfe duyarlı karşılaştırmayı; false, büyük/küçük harfe duyarsız karşılaştırmayı gösterir. |
| [get_ReplacementFormat](./get_replacementformat/)() const | Değiştirmenin biçimini belirtir. Varsayılan değer [Text](../replacementformat/). |
| [get_ReplacingCallback](./get_replacingcallback/)() const | Her değiştirme gerçekleşmeden önce çağrılan kullanıcı tanımlı yöntem. |
| [get_SmartParagraphBreakReplacement](./get_smartparagraphbreakreplacement/)() const | Paragraf kırılımının, sonraki kardeş paragraf yoksa değiştirilmesine izin verilip verilmediğini gösteren bir boolean değerini alır veya ayarlar. Varsayılan değer **false**. |
| [get_UseLegacyOrder](./get_uselegacyorder/)() const | True, metin kutularını dikkate alarak üstten alta sıralı bir metin araması yapıldığını gösterir. Varsayılan değer **false**. |
| [get_UseSubstitutions](./get_usesubstitutions/)() const | Değiştirme kalıpları içinde ikameleri tanıma ve kullanma durumunu gösteren bir boolean değerini alır veya ayarlar. Varsayılan değer **false**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Direction](./set_direction/)(Aspose::Words::Replacing::FindReplaceDirection) | Değiştirme yönünü seçer. Varsayılan değer [Forward](../findreplacedirection/). |
| [set_FindWholeWordsOnly](./set_findwholewordsonly/)(bool) | [Aspose::Words::Replacing::FindReplaceOptions::get_FindWholeWordsOnly](./get_findwholewordsonly/) için ayarlayıcı. |
| [set_IgnoreDeleted](./set_ignoredeleted/)(bool) | [Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreDeleted](./get_ignoredeleted/) için ayarlayıcı. |
| [set_IgnoreFieldCodes](./set_ignorefieldcodes/)(bool) | [Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFieldCodes](./get_ignorefieldcodes/) için ayarlayıcı. |
| [set_IgnoreFields](./set_ignorefields/)(bool) | [Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFields](./get_ignorefields/) için ayarlayıcı. |
| [set_IgnoreFootnotes](./set_ignorefootnotes/)(bool) | [Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFootnotes](./get_ignorefootnotes/) için ayarlayıcı. |
| [set_IgnoreInserted](./set_ignoreinserted/)(bool) | [Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreInserted](./get_ignoreinserted/) için ayarlayıcı. |
| [set_IgnoreOfficeMath](./set_ignoreofficemath/)(bool) | [Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreOfficeMath](./get_ignoreofficemath/) için ayarlayıcı. |
| [set_IgnoreShapes](./set_ignoreshapes/)(bool) | [Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreShapes](./get_ignoreshapes/) için ayarlayıcı. |
| [set_IgnoreStructuredDocumentTags](./set_ignorestructureddocumenttags/)(bool) | [Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreStructuredDocumentTags](./get_ignorestructureddocumenttags/) için ayarlayıcı. |
| [set_LegacyMode](./set_legacymode/)(bool) | [Aspose::Words::Replacing::FindReplaceOptions::get_LegacyMode](./get_legacymode/) için ayarlayıcı. |
| [set_MatchCase](./set_matchcase/)(bool) | [Aspose::Words::Replacing::FindReplaceOptions::get_MatchCase](./get_matchcase/) için ayarlayıcı. |
| [set_ReplacementFormat](./set_replacementformat/)(Aspose::Words::Replacing::ReplacementFormat) | Değiştirmenin biçimini belirtir. Varsayılan değer [Text](../replacementformat/). |
| [set_ReplacingCallback](./set_replacingcallback/)(const System::SharedPtr\<Aspose::Words::Replacing::IReplacingCallback\>\&) | Her değiştirme gerçekleşmeden önce çağrılan kullanıcı tanımlı yöntem. |
| [set_SmartParagraphBreakReplacement](./set_smartparagraphbreakreplacement/)(bool) | [Aspose::Words::Replacing::FindReplaceOptions::get_SmartParagraphBreakReplacement](./get_smartparagraphbreakreplacement/) için ayarlayıcı. |
| [set_UseLegacyOrder](./set_uselegacyorder/)(bool) | True, metin kutularını dikkate alarak üstten alta sıralı bir metin araması yapıldığını gösterir. Varsayılan değer **false**. |
| [set_UseSubstitutions](./set_usesubstitutions/)(bool) | [Aspose::Words::Replacing::FindReplaceOptions::get_UseSubstitutions](./get_usesubstitutions/) için ayarlayıcı. |
| static [Type](./type/)() |  |

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

## Ayrıca Bakınız

* Namespace [Aspose::Words::Replacing](../)
* Library [Aspose.Words for C++](../../)
