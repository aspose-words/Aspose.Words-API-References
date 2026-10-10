---
title: "Aspose::Words::Style::get_List yöntemi"
linktitle: "get_List"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Style::get_List yöntemi. Bu liste stilinin biçimlendirmesini tanımlayan listeyi C++'ta alır."
type: docs
weight: 12000
url: /tr/cpp/aspose.words/style/get_list/
---
## Style::get_List method


Bu liste stilinin biçimlendirmesini tanımlayan listeyi alır.

```cpp
System::SharedPtr<Aspose::Words::Lists::List> Aspose::Words::Style::get_List()
```

## Açıklamalar


Bu özellik yalnızca liste stilleri için geçerlidir. Diğer stil türleri için bu özellik **null** döndürür.

## Örnekler



Bir liste stilini nasıl oluşturup bir belgede kullanacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Bir liste, paragraf gruplarını ön ek sembolleri ve girintilerle düzenlememizi ve süslememizi sağlar.
// Girintiyi artırarak iç içe listeler oluşturabiliriz.
// Bir belge oluşturucunun "ListFormat" özelliğini kullanarak bir listeyi başlatabilir ve sonlandırabiliriz.
// Bir listenin başlangıcı ile sonu arasına eklediğimiz her paragraf, listenin bir öğesi haline gelir.
// Bir stil içinde tüm bir List nesnesi içerebiliriz.
System::SharedPtr<Aspose::Words::Style> listStyle = doc->get_Styles()->Add(Aspose::Words::StyleType::List, u"MyListStyle");

System::SharedPtr<Aspose::Words::Lists::List> list1 = listStyle->get_List();

ASSERT_TRUE(list1->get_IsListStyleDefinition());
ASSERT_FALSE(list1->get_IsListStyleReference());
ASSERT_TRUE(list1->get_IsMultiLevel());
ASPOSE_ASSERT_EQ(listStyle, list1->get_Style());

// Listemizdeki tüm liste seviyelerinin görünümünü değiştirin.
for (auto&& level : list1->get_ListLevels())
{
    level->get_Font()->set_Name(u"Verdana");
    level->get_Font()->set_Color(System::Drawing::Color::get_Blue());
    level->get_Font()->set_Bold(true);
}

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Using list style first time:");

// Bir stil içindeki listeden başka bir liste oluşturun.
System::SharedPtr<Aspose::Words::Lists::List> list2 = doc->get_Lists()->Add(listStyle);

ASSERT_FALSE(list2->get_IsListStyleDefinition());
ASSERT_TRUE(list2->get_IsListStyleReference());
ASPOSE_ASSERT_EQ(listStyle, list2->get_Style());

// Listemizin biçimlendireceği bazı liste öğeleri ekleyin.
builder->get_ListFormat()->set_List(list2);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");
builder->get_ListFormat()->RemoveNumbers();

builder->Writeln(u"Using list style second time:");

// Liste stiline dayanarak başka bir liste oluşturun ve uygulayın.
System::SharedPtr<Aspose::Words::Lists::List> list3 = doc->get_Lists()->Add(listStyle);
builder->get_ListFormat()->set_List(list3);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");
builder->get_ListFormat()->RemoveNumbers();

builder->get_Document()->Save(get_ArtifactsDir() + u"Lists.CreateAndUseListStyle.docx");
```

## Ayrıca Bakınız

* Class [List](../../../aspose.words.lists/list/)
* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
