---
title: "Aspose::Words::Lists::ListFormat sınıfı"
linktitle: "ListFormat"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Lists::ListFormat sınıfı. Bir paragrafa uygulanan liste biçimlendirmesini kontrol etmenizi sağlar. Daha fazla bilgi için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.lists/listformat/
---
## ListFormat class


Bir paragraf için hangi liste biçimlendirmesinin uygulanacağını kontrol etmeyi sağlar. Daha fazla bilgi için, [Working with Lists](https://docs.aspose.com/words/cpp/working-with-lists/) dokümantasyon makalesini ziyaret edin.

```cpp
class ListFormat : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [ApplyBulletDefault](./applybulletdefault/)() | Yeni bir varsayılan madde işaretli liste başlatır ve paragraf üzerine uygular. |
| [ApplyNumberDefault](./applynumberdefault/)() | Yeni bir varsayılan numaralı liste başlatır ve paragrafa uygular. |
| [get_IsListItem](./get_islistitem/)() | Paragrafa madde işaretli veya numaralı biçimlendirme uygulandığında doğru. |
| [get_List](./get_list/)() | Bu paragrafın üyesi olduğu listeyi alır veya ayarlar. |
| [get_ListLevel](./get_listlevel/)() | Liste seviyesi biçimlendirmesini ve geçerli paragrafa uygulanan tüm biçimlendirme geçersiz kılmalarını döndürür. |
| [get_ListLevelNumber](./get_listlevelnumber/)() | Paragraf için liste seviyesi numarasını (0'dan 8'e) alır veya ayarlar. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [ListIndent](./listindent/)() | Geçerli paragrafın liste seviyesini bir seviye artırır. |
| [ListOutdent](./listoutdent/)() | Geçerli paragrafın liste seviyesini bir seviye azaltır. |
| [RemoveNumbers](./removenumbers/)() | Geçerli paragraftan numaraları veya madde işaretlerini kaldırır ve liste seviyesini sıfıra ayarlar. |
| [set_List](./set_list/)(const System::SharedPtr\<Aspose::Words::Lists::List\>\&) | Ayarlayıcı [Aspose::Words::Lists::ListFormat::get_List](./get_list/). |
| [set_ListLevelNumber](./set_listlevelnumber/)(int32_t) | Ayarlayıcı [Aspose::Words::Lists::ListFormat::get_ListLevelNumber](./get_listlevelnumber/). |
| static [Type](./type/)() |  |
## Açıklamalar


Microsoft Word belgesindeki bir paragraf madde işaretli veya numaralı olabilir. Bir paragraf madde işaretli veya numaralı olduğunda, paragrafın liste biçimlendirmesi uygulandığı söylenir.

Doğrudan [ListFormat](./) sınıfının nesnelerini oluşturmazsınız. [ListFormat](./) sınıfına, liste biçimlendirmesiyle ilişkili olabilen başka bir nesnenin özelliği olarak erişirsiniz. Şu anda liste biçimlendirmesine sahip olabilen nesneler şunlardır: [Paragraph](../../aspose.words/paragraph/), [Style](../../aspose.words/style/) ve [DocumentBuilder](../../aspose.words/documentbuilder/).

[ListFormat](./) of a [Paragraph](../../aspose.words/paragraph/) specifies what list formatting and list level is applied to that particular paragraph.

[ListFormat](./) of a [Style](../../aspose.words/style/) (applicable to paragraph styles only) allows to specify what list formatting and list level is applied to all paragraphs of that particular style.

[ListFormat](./) of a [DocumentBuilder](../../aspose.words/documentbuilder/) provides access to the list formatting at the current cursor position inside the [DocumentBuilder](../../aspose.words/documentbuilder/).

Liste biçimlendirmesi kendisi, paragraflardan ayrı olarak depolanan bir [List](../list/) nesnesi içinde saklanır. Liste nesneleri bir [ListCollection](../listcollection/) koleksiyonu içinde saklanır. Her [Document](../../aspose.words/document/) için tek bir [ListCollection](../listcollection/) koleksiyonu bulunur.

Paragraflar fiziksel olarak bir listeye ait değildir. Paragraflar sadece [List](./get_list/) özelliği aracılığıyla belirli bir liste nesnesine ve [ListLevelNumber](./get_listlevelnumber/) özelliği aracılığıyla listedeki belirli bir seviyeye referans verir. Bu iki özelliği ayarlayarak bir paragrafa hangi madde işaretlerinin ve numaralandırmanın uygulanacağını kontrol edersiniz.

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

## Ayrıca Bakınız

* Namespace [Aspose::Words::Lists](../)
* Library [Aspose.Words for C++](../../)
