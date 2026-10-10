---
title: "Aspose::Words::Lists::ListCollection sınıfı"
linktitle: "ListCollection"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Lists::ListCollection sınıfı. Bir belgede kullanılan madde işaretli ve numaralı listelerin biçimlendirmesini depolar ve yönetir. Daha fazla bilgi için C++'daki dokümantasyon makalesini ziyaret edin."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.lists/listcollection/
---
## ListCollection class


Bir belgede kullanılan madde işaretli ve numaralı listelerin biçimlendirmesini depolar ve yönetir. Daha fazla bilgi için, [Working with Lists](https://docs.aspose.com/words/cpp/working-with-lists/) dokümantasyon makalesini ziyaret edin.

```cpp
class ListCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Lists::List>>
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [Add](./add/)(Aspose::Words::Lists::ListTemplate) | Önceden tanımlanmış bir şablona dayalı yeni bir liste oluşturur ve belge içindeki listeler koleksiyonuna ekler. |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | Bir liste stiline referans veren yeni bir liste oluşturur ve belge içindeki listeler koleksiyonuna ekler. |
| [AddCopy](./addcopy/)(const System::SharedPtr\<Aspose::Words::Lists::List\>\&) | Belirtilen listeyi kopyalayarak yeni bir liste oluşturur ve belge içindeki listeler koleksiyonuna ekler. |
| [AddSingleLevelList](./addsinglelevellist/)(Aspose::Words::Lists::ListTemplate) | Önceden tanımlanmış şablona dayalı yeni tek seviyeli bir liste oluşturur ve belge içindeki liste koleksiyonuna ekler. |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Belgedeki numaralı ve madde işaretli listelerin sayısını alır. |
| [get_Document](./get_document/)() const | Sahip belgeyi alır. |
| [GetEnumerator](./getenumerator/)() override | Belgedeki listeleri yineleyecek enumerator nesnesini alır. |
| [GetListByListId](./getlistbylistid/)(int32_t) | Bir liste tanımlayıcısı ile bir liste alır. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Bir indeks ile bir liste alır. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
| [virtualizeBeginConstIterator](./virtualizebeginconstiterator/)() const override |  |
| [virtualizeBeginIterator](./virtualizebeginiterator/)() override |  |
| [virtualizeEndConstIterator](./virtualizeendconstiterator/)() const override |  |
| [virtualizeEndIterator](./virtualizeenditerator/)() override |  |
## Typedefs

| Typedef | Açıklama |
| --- | --- |
| [const_iterator](./const_iterator/) |  |
| [iterator](./iterator/) |  |
| [iterator_holder_type](./iterator_holder_type/) |  |
| [virtualized_iterator](./virtualized_iterator/) |  |
| [virtualized_iterator_element](./virtualized_iterator_element/) |  |
## Açıklamalar


Microsoft Word belgesindeki bir liste, bir dizi liste biçimlendirme özelliğidir. Listelerin biçimlendirmesi, metin paragraflarından ayrı olarak [ListCollection](./) koleksiyonunda depolanır.

Bu sınıfın nesnelerini oluşturmazsınız. Her belge için her zaman yalnızca bir [ListCollection](./) nesnesi bulunur ve bu nesne [Lists](../../aspose.words/documentbase/get_lists/) özelliği aracılığıyla erişilebilir.

Önceden tanımlı bir liste şablonuna veya bir liste stiline dayanarak yeni bir liste oluşturmak için [Add()](../) yöntemini kullanın.

Mevcut bir listeye aynı biçimlendirmeye sahip yeni bir liste oluşturmak için [AddCopy()](../) yöntemini kullanın.

Bir paragrafı madde işaretli veya numaralı yapmak için, bir [List](../list/) nesnesini [ListFormat](../listformat/) nesnesinin [List](../listformat/get_list/) özelliğine atayarak paragrafına liste biçimlendirmesi uygulamanız gerekir.

Bir paragraftan liste biçimlendirmesini kaldırmak için [RemoveNumbers](../listformat/removenumbers/) yöntemini kullanın.

WordprocessingML hakkında biraz bilginiz varsa, \"list\" ve \"list definition\" kavramlarının ayrı tanımlandığını bilebilirsiniz. Bu, liste biçimlendirmesinin bir Microsoft Word belgesinde düşük seviyede nasıl depolandığıyla tam olarak eşleşir. [List](../list/) tanımı bir \"şema\" gibidir ve liste, bir liste tanımının örneği gibidir.

Programlama modelini basitleştirmek için Aspose.Words, Microsoft Word'ün kullanıcı arabiriminde yaptığı gibi liste ile liste tanımı arasındaki farkı gizler. Bu, Microsoft Word dosya formatının gereksinimlerini karşılamak için düşük seviyeli nesneler oluşturmak yerine belgenizin nasıl görünmesini istediğinize daha çok odaklanmanızı sağlar.

Mevcut [Aspose.Words](../../aspose.words/) sürümünde listeler oluşturulduktan sonra silinmesi mümkün değildir. Bu, kullanıcının liste tanımları üzerinde açık bir kontrolü olmadığı Microsoft Word'e benzer.

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
