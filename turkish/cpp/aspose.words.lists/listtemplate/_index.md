---
title: "Aspose::Words::Lists::ListTemplate enum"
linktitle: "ListTemplate"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Lists::ListTemplate enum. Microsoft Word'te C++ için mevcut önceden tanımlanmış liste biçimlerinden birini belirtir."
type: docs
weight: 8000
url: /tr/cpp/aspose.words.lists/listtemplate/
---
## ListTemplate enum


Microsoft Word'de mevcut önceden tanımlı listelerden birini belirtir.

```cpp
enum class ListTemplate
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| BulletDefault | 0 | 9 seviyeli varsayılan madde işaretli liste. İlk seviyenin madde işareti bir disk, ikinci seviyenin madde işareti bir daire, üçüncü seviyenin madde işareti bir kare. Kalan seviyeler için biçimlendirme tekrarlanır. Her seviye, bir önceki seviyeye göre sağa 0.25\" kaydırılır. Microsoft Word'teki Madde İşaretleri ve Numaralandırma iletişim kutusundaki 1. madde işaretli liste şablonuna karşılık gelir. |
| BulletDisk | n/a | Aynı [BulletDefault](./) gibi. Microsoft Word'teki Madde İşaretleri ve Numaralandırma iletişim kutusundaki 1. madde işaretli liste şablonuna karşılık gelir. |
| BulletCircle | n/a | İlk seviyenin madde işareti bir dairedir. Kalan seviyeler [BulletDefault](./) içindekilerle aynıdır. Microsoft Word'teki Madde İşaretleri ve Numaralandırma iletişim kutusundaki 2. madde işaretli liste şablonuna karşılık gelir. |
| BulletSquare | n/a | İlk seviyenin madde işareti bir karedir. Kalan seviyeler [BulletDefault](./) içindekilerle aynıdır. Microsoft Word'teki Madde İşaretleri ve Numaralandırma iletişim kutusundaki 3. madde işaretli liste şablonuna karşılık gelir. |
| BulletDiamonds | n/a | İlk seviyenin madde işareti 4-karo Wingding karakteridir. Kalan seviyeler [BulletDefault](./) içindekilerle aynıdır. Microsoft Word'teki Madde İşaretleri ve Numaralandırma iletişim kutusundaki 5. madde işaretli liste şablonuna karşılık gelir. |
| BulletArrowHead | n/a | İlk seviyenin madde işareti bir ok ucu Wingding karakteridir. Kalan seviyeler [BulletDefault](./) içindekilerle aynıdır. Microsoft Word'teki Madde İşaretleri ve Numaralandırma iletişim kutusundaki 6. madde işaretli liste şablonuna karşılık gelir. |
| BulletTick | n/a | İlk seviyenin madde işareti bir tik Wingding karakteridir. Kalan seviyeler [BulletDefault](./) içindekilerle aynıdır. Microsoft Word'teki Madde İşaretleri ve Numaralandırma iletişim kutusundaki 7. madde işaretli liste şablonuna karşılık gelir. |
| NumberDefault | n/a | 9 seviyeli varsayılan numaralı liste. İlk seviye için Arapça numaralandırma (1., 2., 3., ...), ikinci seviye için küçük harfli harf numaralandırması (a., b., c., ...), üçüncü seviye için küçük harfli Roma rakamı numaralandırması (i., ii., iii., ...). Kalan seviyeler için biçimlendirme tekrarlanır. Her seviye, bir önceki seviyeye göre sağa 0.25\" kaydırılır. Microsoft Word'teki Madde İşaretleri ve Numaralandırma iletişim kutusundaki 1. numaralı liste şablonuna karşılık gelir. |
| NumberArabicDot | n/a | Aynı [NumberDefault](./) gibi. Microsoft Word'teki Madde İşaretleri ve Numaralandırma iletişim kutusundaki 1. numaralı liste şablonuna karşılık gelir. |
| NumberArabicParenthesis | n/a | İlk seviyenin numarası "1)". Kalan seviyeler [NumberDefault](./) içindekilerle aynıdır. Microsoft Word'teki Madde İşaretleri ve Numaralandırma iletişim kutusundaki 2. numaralı liste şablonuna karşılık gelir. |
| NumberUppercaseRomanDot | n/a | İlk seviyenin numarası "I.". Kalan seviyeler [NumberDefault](./) içindekilerle aynıdır. Microsoft Word'teki Madde İşaretleri ve Numaralandırma iletişim kutusundaki 3. numaralı liste şablonuna karşılık gelir. |
| NumberUppercaseLetterDot | n/a | İlk seviyenin numarası "A.". Kalan seviyeler [NumberDefault](./) içindekilerle aynıdır. Microsoft Word'teki Madde İşaretleri ve Numaralandırma iletişim kutusundaki 4. numaralı liste şablonuna karşılık gelir. |
| NumberLowercaseLetterParenthesis | n/a | İlk seviyenin numarası "a)". Kalan seviyeler [NumberDefault](./) içindekilerle aynıdır. Microsoft Word'teki Madde İşaretleri ve Numaralandırma iletişim kutusundaki 5. numaralı liste şablonuna karşılık gelir. |
| NumberLowercaseLetterDot | n/a | İlk seviyenin numarası "a.". Kalan seviyeler [NumberDefault](./) ile aynı. Microsoft Word'deki Madde İşaretleri ve Numaralandırma iletişim kutusundaki 6. numaralı liste şablonuna karşılık gelir. |
| NumberLowercaseRomanDot | n/a | İlk seviyenin numarası "i.". Kalan seviyeler [NumberDefault](./) ile aynı. Microsoft Word'deki Madde İşaretleri ve Numaralandırma iletişim kutusundaki 7. numaralı liste şablonuna karşılık gelir. |
| OutlineNumbers | n/a | Seviyeleri "1), a), i), (1), (a), (i), 1., a., i." şeklinde numaralandırılmış bir anahat listesi. Microsoft Word'deki Madde İşaretleri ve Numaralandırma iletişim kutusundaki 1. anahat liste şablonuna karşılık gelir. |
| OutlineLegal | n/a | Seviyeleri "1., 1.1., 1.1.1, ..." şeklinde numaralandırılmış bir anahat listesi. Microsoft Word'deki Madde İşaretleri ve Numaralandırma iletişim kutusundaki 2. anahat liste şablonuna karşılık gelir. |
| OutlineBullets | n/a | Farklı seviyeler için çeşitli madde işaretlerine sahip bir anahat listesi. Microsoft Word'deki Madde İşaretleri ve Numaralandırma iletişim kutusundaki 3. anahat liste şablonuna karşılık gelir. |
| OutlineHeadingsArticleSection | n/a | Seviyeleri Başlık stillerine bağlanmış bir anahat listesi. Microsoft Word'deki Madde İşaretleri ve Numaralandırma iletişim kutusundaki 4. anahat liste şablonuna karşılık gelir. |
| OutlineHeadingsLegal | n/a | Seviyeleri Başlık stillerine bağlanmış bir anahat listesi. Microsoft Word'deki Madde İşaretleri ve Numaralandırma iletişim kutusundaki 5. anahat liste şablonuna karşılık gelir. |
| OutlineHeadingsNumbers | n/a | Seviyeleri Başlık stillerine bağlanmış bir anahat listesi. Microsoft Word'deki Madde İşaretleri ve Numaralandırma iletişim kutusundaki 6. anahat liste şablonuna karşılık gelir. |
| OutlineHeadingsChapter | n/a | Seviyeleri Başlık stillerine bağlanmış bir anahat listesi. Microsoft Word'deki Madde İşaretleri ve Numaralandırma iletişim kutusundaki 7. anahat liste şablonuna karşılık gelir. |

## Açıklamalar


Bir liste şablonu değeri, [Add()](../listcollection/add/) yöntemine parametre olarak kullanılır.

Aspose.Words liste şablonları, Microsoft Word 2003'teki Madde İşaretleri ve Numaralandırma iletişim kutusunda bulunan 21 liste şablonuna karşılık gelir.

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
