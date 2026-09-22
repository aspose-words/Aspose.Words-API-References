---
title: "Aspose::Words::DocumentBuilder::get_ListFormat yöntemi"
linktitle: "get_ListFormat"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::DocumentBuilder::get_ListFormat yöntemi. C++'ta mevcut liste biçimlendirme özelliklerini temsil eden bir nesne döndürür."
type: docs
weight: 22000
url: /tr/cpp/aspose.words/documentbuilder/get_listformat/
---
## DocumentBuilder::get_ListFormat method


Geçerli liste biçimlendirme özelliklerini temsil eden bir nesne döndürür.

```cpp
System::SharedPtr<Aspose::Words::Lists::ListFormat> Aspose::Words::DocumentBuilder::get_ListFormat()
```


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

## Ayrıca Bakınız

* Class [ListFormat](../../../aspose.words.lists/listformat/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
