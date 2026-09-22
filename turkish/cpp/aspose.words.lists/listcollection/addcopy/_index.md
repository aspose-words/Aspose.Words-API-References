---
title: "Aspose::Words::Lists::ListCollection::AddCopy yöntemi"
linktitle: "AddCopy"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Lists::ListCollection::AddCopy yöntemi. Belirtilen listeyi kopyalayarak yeni bir liste oluşturur ve belge içindeki liste koleksiyonuna ekler C++'ta."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.lists/listcollection/addcopy/
---
## ListCollection::AddCopy method


Belirtilen listeyi kopyalayarak yeni bir liste oluşturur ve belge içindeki listeler koleksiyonuna ekler.

```cpp
System::SharedPtr<Aspose::Words::Lists::List> Aspose::Words::Lists::ListCollection::AddCopy(const System::SharedPtr<Aspose::Words::Lists::List> &srcList)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| srcList | const System::SharedPtr\<Aspose::Words::Lists::List\>\& | Kopyalanacak kaynak liste. |

### ReturnValue

Yeni oluşturulan liste.
## Açıklamalar


Kaynak liste herhangi bir belgeden olabilir. Kaynak liste farklı bir belgeye aitse, listenin bir kopyası oluşturulur ve geçerli belgeye eklenir.

Kaynak liste bir liste stiline referans veya tanım ise, yeni oluşturulan liste orijinal liste stiliyle ilişkili değildir.

## Örnekler



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

* Class [List](../../list/)
* Class [ListCollection](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
