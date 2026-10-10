---
title: "Aspose::Words::Lists::List class"
linktitle: "List"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Lists::List sınıfı. Bir listenin biçimlendirmesini temsil eder. Daha fazla bilgi edinmek için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 1000
url: /tr/cpp/aspose.words.lists/list/
---
## List class


Bir listenin biçimlendirmesini temsil eder. Daha fazla bilgi için, [Working with Lists](https://docs.aspose.com/words/cpp/working-with-lists/) dokümantasyon makalesini ziyaret edin.

```cpp
class List : public System::IComparable<System::SharedPtr<Aspose::Words::Lists::List>>
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [CompareTo](./compareto/)(System::SharedPtr\<Aspose::Words::Lists::List\>) override | Belirtilen listeyi mevcut listeyle karşılaştırır. |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::Lists::List\>\&) | Belirtilen listeyle karşılaştırır. |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | Belirtilen nesnenin mevcut nesneyle değer olarak eşit olup olmadığını belirler. |
| [get_Document](./get_document/)() const | Sahip belgeyi alır. |
| [get_IsListStyleDefinition](./get_isliststyledefinition/)() | Bu liste bir liste stilinin tanımıysa **true** döndürür. |
| [get_IsListStyleReference](./get_isliststylereference/)() | Bu liste bir liste stiline referans ise **true** döndürür. |
| [get_IsMultiLevel](./get_ismultilevel/)() | Liste 9 seviyeye sahipse **true**, 1 seviyeye sahipse **false** döndürür. |
| [get_IsRestartAtEachSection](./get_isrestartateachsection/)() | Listenin her bölümde yeniden başlatılıp başlatılmayacağını belirtir. Varsayılan değer **false**. |
| [get_ListId](./get_listid/)() const | Listenin benzersiz tanımlayıcısını alır. |
| [get_ListLevels](./get_listlevels/)() | Bu listenin liste seviyeleri koleksiyonunu alır. |
| [get_Style](./get_style/)() | Bu listenin referans verdiği veya tanımladığı liste stilini alır. |
| [GetHashCode](./gethashcode/)() const override | Bu liste nesnesi için hash kodunu hesaplar. |
| [GetType](./gettype/)() const override |  |
| [HasSameTemplate](./hassametemplate/)(const System::SharedPtr\<Aspose::Words::Lists::List\>\&) | Mevcut liste ve verilen listenin aynı şablondan oluşturulmuş olması durumunda true döndürür. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_IsRestartAtEachSection](./set_isrestartateachsection/)(bool) | Ayarlayıcı: [Aspose::Words::Lists::List::get_IsRestartAtEachSection](./get_isrestartateachsection/). |
| static [Type](./type/)() |  |
## Açıklamalar


Microsoft Word belgesindeki bir liste, bir dizi liste biçimlendirme özelliğidir. Her liste en fazla 9 seviyeye sahip olabilir ve sayı stili, başlangıç değeri, girinti, sekme konumu vb. gibi biçimlendirme özellikleri her seviye için ayrı ayrı tanımlanır.

Bir [List](./) nesnesi her zaman [ListCollection](../listcollection/) koleksiyonuna aittir.

Yeni bir liste oluşturmak için, [ListCollection](../listcollection/) koleksiyonunun Add yöntemlerini kullanın.

Bir listenin biçimlendirmesini değiştirmek için, [ListLevels](./get_listlevels/) koleksiyonunda bulunan [ListLevel](../listlevel/) nesnelerini kullanın.

Bir paragraftan liste biçimlendirmesini uygulamak veya kaldırmak için [ListFormat](../listformat/) kullanın.

## Örnekler



Liste seviyeleriyle nasıl çalışılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

ASSERT_FALSE(builder->get_ListFormat()->get_IsListItem());

// Bir liste, paragraf gruplarını ön ek sembolleri ve girintilerle düzenlememizi ve süslememizi sağlar.
// Girintiyi artırarak iç içe listeler oluşturabiliriz.
// Bir belge oluşturucunun "ListFormat" özelliğini kullanarak bir listeyi başlatabilir ve sonlandırabiliriz.
// Bir listenin başlangıcı ile sonu arasına eklediğimiz her paragraf, listenin bir öğesi haline gelir.
// Aşağıda, bir belge oluşturucu kullanarak oluşturabileceğimiz iki tür liste bulunmaktadır.
// 1 -  Numaranmış bir liste:
// Numaralı listeler, her öğeyi numaralandırarak paragrafları için mantıksal bir sıra oluşturur.
builder->get_ListFormat()->set_List(doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault));

ASSERT_TRUE(builder->get_ListFormat()->get_IsListItem());

// "ListLevelNumber" özelliğini ayarlayarak, liste seviyesini artırabiliriz
// geçerli liste öğesinde bağımsız bir alt liste başlatmak için.
// "NumberDefault" adlı Microsoft Word liste şablonu, ilk liste seviyesi için liste seviyeleri oluşturmak amacıyla sayıları kullanır.
// Daha derin liste seviyeleri harfler ve küçük harf Roma rakamları kullanır.
for (int32_t i = 0; i < 9; i++)
{
    builder->get_ListFormat()->set_ListLevelNumber(i);
    builder->Writeln(System::String(u"Level ") + i);
}

// 2 -  Bir madde işaretli liste:
// Bu liste, her paragraftan önce bir girinti ve madde işareti ("•") uygular.
// Bu listenin daha derin seviyeleri, "■" ve "○" gibi farklı semboller kullanacaktır.
builder->get_ListFormat()->set_List(doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::BulletDefault));

for (int32_t i = 0; i < 9; i++)
{
    builder->get_ListFormat()->set_ListLevelNumber(i);
    builder->Writeln(System::String(u"Level ") + i);
}

// "List" bayrağını kaldırarak, sonraki paragrafların listeler gibi biçimlendirilmemesi için liste biçimlendirmesini devre dışı bırakabiliriz.
builder->get_ListFormat()->set_List(nullptr);

ASSERT_FALSE(builder->get_ListFormat()->get_IsListItem());

doc->Save(get_ArtifactsDir() + u"Lists.SpecifyListLevel.docx");
```


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


Bir listeyi kopyalayarak numaralandırmayı nasıl yeniden başlatacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Bir liste, paragraf gruplarını ön ek sembolleri ve girintilerle düzenlememizi ve süslememizi sağlar.
// Girintiyi artırarak iç içe listeler oluşturabiliriz.
// Bir belge oluşturucunun "ListFormat" özelliğini kullanarak bir listeyi başlatabilir ve sonlandırabiliriz.
// Bir listenin başlangıcı ile sonu arasına eklediğimiz her paragraf, listenin bir öğesi haline gelir.
// Microsoft Word şablonundan bir liste oluşturun ve ilk liste seviyesini özelleştirin.
System::SharedPtr<Aspose::Words::Lists::List> list1 = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberArabicParenthesis);
list1->get_ListLevels()->idx_get(0)->get_Font()->set_Color(System::Drawing::Color::get_Red());
list1->get_ListLevels()->idx_get(0)->set_Alignment(Aspose::Words::Lists::ListLevelAlignment::Right);

// Listemizi bazı paragraflara uygulayın.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"List 1 starts below:");
builder->get_ListFormat()->set_List(list1);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");
builder->get_ListFormat()->RemoveNumbers();

// Mevcut bir listenin bir kopyasını belgenin liste koleksiyonuna ekleyebiliriz
// orijinali değiştirmeden benzer bir liste oluşturmak için.
System::SharedPtr<Aspose::Words::Lists::List> list2 = doc->get_Lists()->AddCopy(list1);
list2->get_ListLevels()->idx_get(0)->get_Font()->set_Color(System::Drawing::Color::get_Blue());
list2->get_ListLevels()->idx_get(0)->set_StartAt(10);

// İkinci listeyi yeni paragraflara uygulayın.
builder->Writeln(u"List 2 starts below:");
builder->get_ListFormat()->set_List(list2);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");
builder->get_ListFormat()->RemoveNumbers();

doc->Save(get_ArtifactsDir() + u"Lists.RestartNumberingUsingListCopy.docx");
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Lists](../)
* Library [Aspose.Words for C++](../../)
