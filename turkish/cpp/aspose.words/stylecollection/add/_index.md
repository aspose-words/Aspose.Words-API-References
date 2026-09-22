---
title: "Aspose::Words::StyleCollection::Add metodu"
linktitle: "Add"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::StyleCollection::Add metodu. C++'ta yeni bir kullanıcı tanımlı stil oluşturur ve koleksiyona ekler."
type: docs
weight: 2000
url: /tr/cpp/aspose.words/stylecollection/add/
---
## StyleCollection::Add method


Yeni bir kullanıcı tanımlı stil oluşturur ve koleksiyona ekler.

```cpp
System::SharedPtr<Aspose::Words::Style> Aspose::Words::StyleCollection::Add(Aspose::Words::StyleType type, const System::String &name)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| type | Aspose::Words::StyleType | Oluşturulacak stilin türünü belirten bir [StyleType](../../styletype/) değeri. |
| name | const System::String\& | Oluşturulacak stilin büyük/küçük harfe duyarlı adı. |
## Açıklamalar


Karakter, paragraf veya liste stili oluşturabilirsiniz.

Liste stili oluştururken, stil varsayılan numaralı liste biçimi (1 \ a \ i) ile oluşturulur.

Bu adla bir stil zaten mevcutsa bir istisna fırlatır.

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


Bir belgenin stil koleksiyonuna bir [Style](../../style/) nasıl eklenir gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::StyleCollection> styles = doc->get_Styles();
// Bu koleksiyona daha sonra ekleyebileceğimiz yeni stiller için varsayılan parametreleri ayarlayın.
styles->get_DefaultFont()->set_Name(u"Courier New");
// Eğer "StyleType.Paragraph" stilini eklersek, koleksiyon değerlerini uygular
// "DefaultParagraphFormat" özelliğini stilin "ParagraphFormat" özelliğine.
styles->get_DefaultParagraphFormat()->set_FirstLineIndent(15.0);
// Bir stil ekleyin ve ardından varsayılan ayarları içerdiğini doğrulayın.
styles->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle");

ASSERT_EQ(u"Courier New", styles->idx_get(4)->get_Font()->get_Name());
ASPOSE_ASSERT_EQ(15.0, styles->idx_get(u"MyStyle")->get_ParagraphFormat()->get_FirstLineIndent());
```

## Ayrıca Bakınız

* Class [Style](../../style/)
* Enum [StyleType](../../styletype/)
* Class [StyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
