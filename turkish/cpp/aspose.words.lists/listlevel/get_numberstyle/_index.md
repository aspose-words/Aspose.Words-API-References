---
title: "Aspose::Words::Lists::ListLevel::get_NumberStyle metodu"
linktitle: "get_NumberStyle"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Lists::ListLevel::get_NumberStyle metodu. C++'ta bu liste seviyesi için sayı stilini döndürür veya ayarlar."
type: docs
weight: 14000
url: /tr/cpp/aspose.words.lists/listlevel/get_numberstyle/
---
## ListLevel::get_NumberStyle method


Bu liste seviyesi için sayı stilini döndürür veya ayarlar.

```cpp
Aspose::Words::NumberStyle Aspose::Words::Lists::ListLevel::get_NumberStyle() const
```


## Örnekler



Shows how to apply custom list formatting to paragraphs when using [DocumentBuilder](../../../aspose.words/documentbuilder/).
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


Özel liste etiketlerini özelleştirmenin gelişmiş yollarını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Bir liste, paragraf gruplarını ön ek sembolleri ve girintilerle düzenlememizi ve süslememizi sağlar.
// Girintiyi artırarak iç içe listeler oluşturabiliriz.
// Bir belge oluşturucunun "ListFormat" özelliğini kullanarak bir listeyi başlatabilir ve sonlandırabiliriz.
// Bir listenin başlangıcı ile sonu arasına eklediğimiz her paragraf, listenin bir öğesi haline gelir.
System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault);

// Seviye 1 etiketleri "Heading 1" paragraf stiline göre biçimlendirilecek ve bir önek alacak.
// Bunlar "Appendix A", "Appendix B" gibi görünecek...
list->get_ListLevels()->idx_get(0)->set_NumberFormat(u"Appendix \x0000");
list->get_ListLevels()->idx_get(0)->set_NumberStyle(Aspose::Words::NumberStyle::UppercaseLetter);
list->get_ListLevels()->idx_get(0)->set_LinkedStyle(doc->get_Styles()->idx_get(u"Heading 1"));

// Seviye 2 etiketleri birinci ve ikinci liste seviyelerinin mevcut sayılarını gösterecek ve başında sıfırlar bulunacak.
// İlk liste seviyesi 1 ise, bu etiketler "Section (1.01)", "Section (1.02)" gibi görünecek...
list->get_ListLevels()->idx_get(1)->set_NumberFormat(u"Section (\x0000" u".\x0001" u")");
list->get_ListLevels()->idx_get(1)->set_NumberStyle(Aspose::Words::NumberStyle::LeadingZero);

// Üst seviyenin UppercaseLetter numaralandırmasını kullandığını unutmayın.
// "IsLegal" özelliğini ayarlayarak üst liste seviyeleri için Arap rakamları kullanabiliriz.
list->get_ListLevels()->idx_get(1)->set_IsLegal(true);
list->get_ListLevels()->idx_get(1)->set_RestartAfterLevel(0);

// Seviye 3 etiketleri bir önek ve sonek ile büyük harf Roma rakamları olacak ve her Liste seviyesi 1 öğesinde yeniden başlayacak.
// Bu liste etiketleri "-I-", "-II-" gibi görünecek...
list->get_ListLevels()->idx_get(2)->set_NumberFormat(u"-\x0002" u"-");
list->get_ListLevels()->idx_get(2)->set_NumberStyle(Aspose::Words::NumberStyle::UppercaseRoman);
list->get_ListLevels()->idx_get(2)->set_RestartAfterLevel(1);

// Tüm liste seviyelerinin etiketlerini kalın yap.
for (auto&& level : list->get_ListLevels())
{
    level->get_Font()->set_Bold(true);
}

// Mevcut paragraf için liste biçimlendirmesini uygula.
builder->get_ListFormat()->set_List(list);

// Üç liste seviyemizi de gösterecek liste öğeleri oluştur.
for (int32_t n = 0; n < 2; n++)
{
    for (int32_t i = 0; i < 3; i++)
    {
        builder->get_ListFormat()->set_ListLevelNumber(i);
        builder->Writeln(System::String(u"Level ") + i);
    }
}

builder->get_ListFormat()->RemoveNumbers();

doc->Save(get_ArtifactsDir() + u"Lists.CreateListRestartAfterHigher.docx");
```

## Ayrıca Bakınız

* Enum [NumberStyle](../../../aspose.words/numberstyle/)
* Class [ListLevel](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
