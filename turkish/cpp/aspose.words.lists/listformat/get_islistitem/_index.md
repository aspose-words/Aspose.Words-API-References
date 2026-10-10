---
title: "Aspose::Words::Lists::ListFormat::get_IsListItem yöntemi"
linktitle: "get_IsListItem"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Lists::ListFormat::get_IsListItem yöntemi. C++'ta paragrafın madde işareti veya numaralı biçimlendirme almış olması durumunda doğru döner."
type: docs
weight: 4000
url: /tr/cpp/aspose.words.lists/listformat/get_islistitem/
---
## ListFormat::get_IsListItem method


Paragrafa madde işaretli veya numaralı biçimlendirme uygulandığında doğru.

```cpp
bool Aspose::Words::Lists::ListFormat::get_IsListItem()
```


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


Bir belgede liste öğesi olan tüm paragrafların nasıl çıktılanacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_ListFormat()->ApplyNumberDefault();
builder->Writeln(u"Numbered list item 1");
builder->Writeln(u"Numbered list item 2");
builder->Writeln(u"Numbered list item 3");
builder->get_ListFormat()->RemoveNumbers();

builder->get_ListFormat()->ApplyBulletDefault();
builder->Writeln(u"Bulleted list item 1");
builder->Writeln(u"Bulleted list item 2");
builder->Writeln(u"Bulleted list item 3");
builder->get_ListFormat()->RemoveNumbers();

System::SharedPtr<Aspose::Words::NodeCollection> paras = doc->GetChildNodes(Aspose::Words::NodeType::Paragraph, true);

for (auto&& para : paras->LINQ_OfType<System::SharedPtr<Aspose::Words::Paragraph> >()->LINQ_Where(static_cast<System::Func<System::SharedPtr<Aspose::Words::Paragraph>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Paragraph> p)>>([](System::SharedPtr<Aspose::Words::Paragraph> p) -> bool
{
    return p->get_ListFormat()->get_IsListItem();
})))->LINQ_ToList())
{
    std::cout << System::String::Format(u"This paragraph belongs to list ID# {0}, number style \"{1}\"", para->get_ListFormat()->get_List()->get_ListId(), para->get_ListFormat()->get_ListLevel()->get_NumberStyle()) << std::endl;
    std::cout << System::String::Format(u"\t\"{0}\"", para->GetText().Trim()) << std::endl;
}
```

## Ayrıca Bakınız

* Class [ListFormat](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
