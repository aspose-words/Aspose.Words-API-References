---
title: "Aspose::Words::Markup::CustomXmlPropertyCollection::idx_get method"
linktitle: "idx_get"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Markup::CustomXmlPropertyCollection::idx_get metodu. C++'da belirtilen isimde bir özelliği alır."
type: docs
weight: 8000
url: /tr/cpp/aspose.words.markup/customxmlpropertycollection/idx_get/
---
## CustomXmlPropertyCollection::idx_get(const System::String\&) method


Belirtilen ada sahip bir özelliği alır.

```cpp
System::SharedPtr<Aspose::Words::Markup::CustomXmlProperty> Aspose::Words::Markup::CustomXmlPropertyCollection::idx_get(const System::String &name)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| name | const System::String\& | Bulunacak özelliğin büyük/küçük harfe duyarlı adı. |

## Örnekler



Akıllı etiket özellikleriyle nasıl çalışılacağını göstererek akıllı etiketler hakkında ayrıntılı bilgi almanızı sağlar.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Smart tags.doc");

// Microsoft Word, bir belgedeki metnin bir kısmını bir veri biçimi olarak tanıdığında bir akıllı etiket ortaya çıkar,
// örneğin bir isim, tarih veya adres gibi ve bunu mor noktalı altı çizili bir köprüye dönüştürür.
// Word 2003'te, akıllı etiketleri \"Tools\" -> \"AutoCorrect options...\" -> \"SmartTags\" yoluyla etkinleştirebiliriz.
// Girdi belgemizde, Microsoft Word tarafından akıllı etiket olarak kaydedilen üç nesne var.
// Akıllı etiketler iç içe olabilir, bu yüzden bu koleksiyon daha fazlasını içerir.
System::ArrayPtr<System::SharedPtr<Aspose::Words::Markup::SmartTag>> smartTags = doc->GetChildNodes(Aspose::Words::NodeType::SmartTag, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Markup::SmartTag> >()->LINQ_ToArray();

ASSERT_EQ(8, smartTags->get_Length());

// \"Properties\" üyesi bir akıllı etiketin meta verilerini içerir ve bu, her akıllı etiket türü için farklı olacaktır.
// \"date\" türündeki bir akıllı etiketin özellikleri yıl, ay ve günü içerir.
System::SharedPtr<Aspose::Words::Markup::CustomXmlPropertyCollection> properties = smartTags[7]->get_Properties();

ASSERT_EQ(4, properties->get_Count());

{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Markup::CustomXmlProperty>>> enumerator = properties->GetEnumerator();
    while (enumerator->MoveNext())
    {
        std::cout << System::String::Format(u"Property name: {0}, value: {1}", enumerator->get_Current()->get_Name(), enumerator->get_Current()->get_Value()) << std::endl;
        ASSERT_EQ(u"", enumerator->get_Current()->get_Uri());
    }
}

// Ayrıca özelliklere çeşitli yollarla, örneğin bir anahtar-değer çifti gibi erişebiliriz.
ASSERT_TRUE(properties->Contains(u"Day"));
ASSERT_EQ(u"22", properties->idx_get(u"Day")->get_Value());
ASSERT_EQ(u"2003", properties->idx_get(2)->get_Value());
ASSERT_EQ(1, properties->IndexOfKey(u"Month"));

// Aşağıda, özellikler koleksiyonundan öğeleri kaldırmanın üç yolu verilmiştir.
// 1 -  İndekse göre kaldır:
properties->RemoveAt(3);

ASSERT_EQ(3, properties->get_Count());

// 2 -  İsme göre kaldır:
properties->Remove(u"Year");

ASSERT_EQ(2, properties->get_Count());

// 3 -  Tüm koleksiyonu bir kerede temizle:
properties->Clear();

ASSERT_EQ(0, properties->get_Count());
```

## Ayrıca Bakınız

* Class [CustomXmlProperty](../../customxmlproperty/)
* Class [CustomXmlPropertyCollection](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
## CustomXmlPropertyCollection::idx_get(int32_t) method


Belirtilen indeksteki bir özelliği alır.

```cpp
System::SharedPtr<Aspose::Words::Markup::CustomXmlProperty> Aspose::Words::Markup::CustomXmlPropertyCollection::idx_get(int32_t index)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| index | int32_t | Özelliğin sıfır tabanlı indeksi. |

## Örnekler



Akıllı etiket özellikleriyle nasıl çalışılacağını göstererek akıllı etiketler hakkında ayrıntılı bilgi almanızı sağlar.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Smart tags.doc");

// Microsoft Word, bir belgedeki metnin bir kısmını bir veri biçimi olarak tanıdığında bir akıllı etiket ortaya çıkar,
// örneğin bir isim, tarih veya adres gibi ve bunu mor noktalı altı çizili bir köprüye dönüştürür.
// Word 2003'te, akıllı etiketleri \"Tools\" -> \"AutoCorrect options...\" -> \"SmartTags\" yoluyla etkinleştirebiliriz.
// Girdi belgemizde, Microsoft Word tarafından akıllı etiket olarak kaydedilen üç nesne var.
// Akıllı etiketler iç içe olabilir, bu yüzden bu koleksiyon daha fazlasını içerir.
System::ArrayPtr<System::SharedPtr<Aspose::Words::Markup::SmartTag>> smartTags = doc->GetChildNodes(Aspose::Words::NodeType::SmartTag, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Markup::SmartTag> >()->LINQ_ToArray();

ASSERT_EQ(8, smartTags->get_Length());

// \"Properties\" üyesi bir akıllı etiketin meta verilerini içerir ve bu, her akıllı etiket türü için farklı olacaktır.
// \"date\" türündeki bir akıllı etiketin özellikleri yıl, ay ve günü içerir.
System::SharedPtr<Aspose::Words::Markup::CustomXmlPropertyCollection> properties = smartTags[7]->get_Properties();

ASSERT_EQ(4, properties->get_Count());

{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Markup::CustomXmlProperty>>> enumerator = properties->GetEnumerator();
    while (enumerator->MoveNext())
    {
        std::cout << System::String::Format(u"Property name: {0}, value: {1}", enumerator->get_Current()->get_Name(), enumerator->get_Current()->get_Value()) << std::endl;
        ASSERT_EQ(u"", enumerator->get_Current()->get_Uri());
    }
}

// Ayrıca özelliklere çeşitli yollarla, örneğin bir anahtar-değer çifti gibi erişebiliriz.
ASSERT_TRUE(properties->Contains(u"Day"));
ASSERT_EQ(u"22", properties->idx_get(u"Day")->get_Value());
ASSERT_EQ(u"2003", properties->idx_get(2)->get_Value());
ASSERT_EQ(1, properties->IndexOfKey(u"Month"));

// Aşağıda, özellikler koleksiyonundan öğeleri kaldırmanın üç yolu verilmiştir.
// 1 -  İndekse göre kaldır:
properties->RemoveAt(3);

ASSERT_EQ(3, properties->get_Count());

// 2 -  İsme göre kaldır:
properties->Remove(u"Year");

ASSERT_EQ(2, properties->get_Count());

// 3 -  Tüm koleksiyonu bir kerede temizle:
properties->Clear();

ASSERT_EQ(0, properties->get_Count());
```

## Ayrıca Bakınız

* Class [CustomXmlProperty](../../customxmlproperty/)
* Class [CustomXmlPropertyCollection](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
