---
title: "Aspose::Words::Lists::ListFormat::get_ListLevelNumber method"
linktitle: "get_ListLevelNumber"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Lists::ListFormat::get_ListLevelNumber yöntemi. C++'ta paragraf için liste seviyesi numarasını (0'dan 8'e) alır veya ayarlar."
type: docs
weight: 7000
url: /tr/cpp/aspose.words.lists/listformat/get_listlevelnumber/
---
## ListFormat::get_ListLevelNumber method


Paragraf için liste seviyesi numarasını (0'dan 8'e) alır veya ayarlar.

```cpp
int32_t Aspose::Words::Lists::ListFormat::get_ListLevelNumber()
```

## Açıklamalar


Word belgelerinde listeler 1 ila 9 seviye içerebilir ve 0'dan 8'e kadar numaralandırılır.

Yalnızca [List](../get_list/) özelliği geçerli bir listeye referans vermek üzere ayarlandığında etkili olur.

## Örnekler



Madde işaretli ve numaralı listelerin nasıl oluşturulacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Aspose.Words main advantages are:");

// Bir liste, paragraf gruplarını ön ek sembolleri ve girintilerle düzenlememizi ve süslememizi sağlar.
// Girintiyi artırarak iç içe listeler oluşturabiliriz.
// Bir belge oluşturucunun "ListFormat" özelliğini kullanarak bir listeyi başlatabilir ve sonlandırabiliriz.
// Bir listenin başlangıcı ile sonu arasına eklediğimiz her paragraf, listenin bir öğesi haline gelir.
// Aşağıda bir belge oluşturucu ile oluşturabileceğimiz iki tür liste bulunmaktadır.
// 1 -  Bir madde işaretli liste:
// Bu liste, her paragraftan önce bir girinti ve madde işareti ("•") uygular.
builder->get_ListFormat()->ApplyBulletDefault();
builder->Writeln(u"Great performance");
builder->Writeln(u"High reliability");
builder->Writeln(u"Quality code and working");
builder->Writeln(u"Wide variety of features");
builder->Writeln(u"Easy to understand API");

// Madde işaretli listeyi sonlandır.
builder->get_ListFormat()->RemoveNumbers();

builder->InsertBreak(Aspose::Words::BreakType::ParagraphBreak);
builder->Writeln(u"Aspose.Words allows:");

// 2 -  Bir numaralı liste:
// Numaralı listeler, her öğeyi numaralandırarak paragrafları için mantıksal bir sıra oluşturur.
builder->get_ListFormat()->ApplyNumberDefault();

// Bu paragraf ilk öğedir. Numaralı bir listenin ilk öğesi "1." sembolüne sahip olacaktır.
builder->Writeln(u"Opening documents from different formats:");

ASSERT_EQ(0, builder->get_ListFormat()->get_ListLevelNumber());

// Mevcut liste seviyesini artırmak için "ListIndent" yöntemini çağırın,
// Bu, birinci liste seviyesindeki mevcut öğede daha derin bir girinti ile yeni, bağımsız bir liste başlatacaktır.
builder->get_ListFormat()->ListIndent();

ASSERT_EQ(1, builder->get_ListFormat()->get_ListLevelNumber());

// Bunlar, ikinci liste seviyesinin ilk üç liste öğesidir ve bir sayımı koruyacaktır
// birinci liste seviyesinin sayımından bağımsızdır. Mevcut liste formatına göre,
// "a.", "b." ve "c." sembollerine sahip olacaklardır.
builder->Writeln(u"DOC");
builder->Writeln(u"PDF");
builder->Writeln(u"HTML");

// Önceki liste seviyesine dönmek için "ListOutdent" yöntemini çağırın.
builder->get_ListFormat()->ListOutdent();

ASSERT_EQ(0, builder->get_ListFormat()->get_ListLevelNumber());

// Bu iki paragraf birinci liste seviyesinin sayımını sürdürecektir.
// Bu öğeler "2." ve "3." sembollerine sahip olacaktır
builder->Writeln(u"Processing documents");
builder->Writeln(u"Saving documents in different formats:");

// Daha önce öğeler eklediğimiz bir seviyeye liste seviyesini artırırsak,
// iç içe liste önceki listeden ayrı olacak ve numaralandırması baştan başlayacaktır.
// Bu liste öğeleri "a.", "b.", "c.", "d." ve "e" sembollerine sahip olacaktır.
builder->get_ListFormat()->ListIndent();
builder->Writeln(u"DOC");
builder->Writeln(u"PDF");
builder->Writeln(u"HTML");
builder->Writeln(u"MHTML");
builder->Writeln(u"Plain text");

// Liste seviyesini tekrar dışarı kaydırın.
builder->get_ListFormat()->ListOutdent();
builder->Writeln(u"Doing many other things!");

// Numaralı listeyi sonlandırın.
builder->get_ListFormat()->RemoveNumbers();

doc->Save(get_ArtifactsDir() + u"Lists.ApplyDefaultBulletsAndNumbers.docx");
```


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

## Ayrıca Bakınız

* Class [ListFormat](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
