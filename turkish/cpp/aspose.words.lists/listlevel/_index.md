---
title: "Aspose::Words::Lists::ListLevel class"
linktitle: "ListLevel"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Lists::ListLevel sınıfı. Bir liste seviyesinin biçimlendirmesini tanımlar. Daha fazla bilgi için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 5000
url: /tr/cpp/aspose.words.lists/listlevel/
---
## ListLevel class


Bir liste seviyesinin biçimlendirmesini tanımlar. Daha fazla bilgi için, [Working with Lists](https://docs.aspose.com/words/cpp/working-with-lists/) dokümantasyon makalesini ziyaret edin.

```cpp
class ListLevel : public Aspose::Words::IRunAttrSource
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [CreatePictureBullet](./createpicturebullet/)() | Geçerli liste seviyesi için resim madde işareti şekli oluşturur. |
| [DeletePictureBullet](./deletepicturebullet/)() | Geçerli liste seviyesi için resim madde işaretini siler. |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::Lists::ListLevel\>\&) | Belirtilen [ListLevel](./) ile karşılaştırır. |
| [get_Alignment](./get_alignment/)() const | Liste öğesinin gerçek numarasının hizalamasını alır veya ayarlar. |
| [get_CustomNumberStyleFormat](./get_customnumberstyleformat/)() | Bu liste seviyesi için özel sayı stili biçimini alır veya ayarlar. Örneğin: "a, ç, ĝ, ...". |
| [get_Font](./get_font/)() | Liste etiketi için kullanılan karakter biçimlendirmesini belirtir. |
| [get_ImageData](./get_imagedata/)() | Geçerli liste seviyesi için resim madde işareti şeklinin görüntü verilerini döndürür. |
| [get_IsLegal](./get_islegal/)() const | Seviye tüm kalıtılmış sayıları Arapça'ya dönüştürüyorsa doğru, sayı stilini koruyorsa yanlış. |
| [get_LinkedStyle](./get_linkedstyle/)() | Bu liste seviyesiyle bağlantılı paragraf stilini alır veya ayarlar. |
| [get_NumberFormat](./get_numberformat/)() const | Liste seviyesi için sayı biçimini döndürür veya ayarlar. |
| [get_NumberPosition](./get_numberposition/)() const | Liste seviyesi için sayı veya madde işaretinin konumunu (puan cinsinden) döndürür veya ayarlar. |
| [get_NumberStyle](./get_numberstyle/)() const | Bu liste seviyesi için sayı stilini döndürür veya ayarlar. |
| [get_RestartAfterLevel](./get_restartafterlevel/)() const | Belirtilen liste seviyesinin numaralandırmayı yeniden başlatmasından önce görünmesi gereken liste seviyesini ayarlar veya döndürür. |
| [get_StartAt](./get_startat/)() | Bu liste seviyesi için başlangıç numarasını döndürür veya ayarlar. |
| [get_TabPosition](./get_tabposition/)() const | Liste seviyesi için sekme konumunu (puan cinsinden) döndürür veya ayarlar. |
| [get_TextPosition](./get_textposition/)() const | Liste seviyesi için sarmalanan metnin ikinci satırının konumunu (puan cinsinden) döndürür veya ayarlar. |
| [get_TrailingCharacter](./get_trailingcharacter/)() const | Liste seviyesi için sayının ardından eklenen karakteri döndürür veya ayarlar. |
| static [GetEffectiveValue](./geteffectivevalue/)(int32_t, Aspose::Words::NumberStyle, const System::String\&) | Belirtilen liste öğesi indeksine ait [ListLevel](./) nesnesinin dize temsilini raporlar. Parametreler, [NumberStyle](../../aspose.words/numberstyle/) ve [Custom](../../aspose.words/numberstyle/) belirtildiğinde kullanılan isteğe bağlı bir biçim dizesini tanımlar. |
| [GetHashCode](./gethashcode/)() const override | Bu nesne için karma kodunu hesaplar. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [RemoveTabStop](./removetabstop/)() | Liste seviyesinden sekme durağını kaldırır. |
| [set_Alignment](./set_alignment/)(Aspose::Words::Lists::ListLevelAlignment) | [Aspose::Words::Lists::ListLevel::get_Alignment](./get_alignment/) için ayarlayıcı. |
| [set_CustomNumberStyleFormat](./set_customnumberstyleformat/)(const System::String\&) | [Aspose::Words::Lists::ListLevel::get_CustomNumberStyleFormat](./get_customnumberstyleformat/) için ayarlayıcı. |
| [set_IsLegal](./set_islegal/)(bool) | [Aspose::Words::Lists::ListLevel::get_IsLegal](./get_islegal/) için ayarlayıcı. |
| [set_LinkedStyle](./set_linkedstyle/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | [Aspose::Words::Lists::ListLevel::get_LinkedStyle](./get_linkedstyle/) için ayarlayıcı. |
| [set_NumberFormat](./set_numberformat/)(const System::String\&) | [Aspose::Words::Lists::ListLevel::get_NumberFormat](./get_numberformat/) için ayarlayıcı. |
| [set_NumberPosition](./set_numberposition/)(double) | [Aspose::Words::Lists::ListLevel::get_NumberPosition](./get_numberposition/) için ayarlayıcı. |
| [set_NumberStyle](./set_numberstyle/)(Aspose::Words::NumberStyle) | [Aspose::Words::Lists::ListLevel::get_NumberStyle](./get_numberstyle/) için ayarlayıcı. |
| [set_RestartAfterLevel](./set_restartafterlevel/)(int32_t) | Ayarlayıcı [Aspose::Words::Lists::ListLevel::get_RestartAfterLevel](./get_restartafterlevel/) için. |
| [set_StartAt](./set_startat/)(int32_t) | Ayarlayıcı [Aspose::Words::Lists::ListLevel::get_StartAt](./get_startat/) için. |
| [set_TabPosition](./set_tabposition/)(double) | Ayarlayıcı [Aspose::Words::Lists::ListLevel::get_TabPosition](./get_tabposition/) için. |
| [set_TextPosition](./set_textposition/)(double) | Ayarlayıcı [Aspose::Words::Lists::ListLevel::get_TextPosition](./get_textposition/) için. |
| [set_TrailingCharacter](./set_trailingcharacter/)(Aspose::Words::Lists::ListTrailingCharacter) | Ayarlayıcı [Aspose::Words::Lists::ListLevel::get_TrailingCharacter](./get_trailingcharacter/) için. |
| static [Type](./type/)() |  |
## Açıklamalar


Bu sınıfın nesnelerini oluşturmazsınız. [List](../list/) seviye nesneleri bir liste oluşturulduğunda otomatik olarak oluşturulur. [ListLevel](./) nesnelerine [ListLevelCollection](../listlevelcollection/) koleksiyonu aracılığıyla erişirsiniz.

Bireysel liste seviyeleri için liste biçimlendirmesini belirtmek üzere [ListLevel](./) özelliklerini kullanın.

## Örnekler



[DocumentBuilder](../../aspose.words/documentbuilder/) kullanırken paragraflara özel liste biçimlendirmesinin nasıl uygulanacağını gösterir.
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

* Namespace [Aspose::Words::Lists](../)
* Library [Aspose.Words for C++](../../)
