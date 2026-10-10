---
title: "Aspose::Words::Bibliography::PersonCollection::PersonCollection yapıcı"
linktitle: "PersonCollection"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Bibliography::PersonCollection::PersonCollection yapıcı. C++'ta PersonCollection sınıfının yeni bir örneğini başlatır."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.bibliography/personcollection/personcollection/
---
## PersonCollection::PersonCollection() constructor


Yeni bir [PersonCollection](../) sınıfı örneği oluştur.

```cpp
Aspose::Words::Bibliography::PersonCollection::PersonCollection()
```


## Örnekler



Kişi koleksiyonu ile nasıl çalışılacağını gösterir.
```cpp
// Yeni bir kişi koleksiyonu oluştur.
auto persons = System::MakeObject<Aspose::Words::Bibliography::PersonCollection>();
auto person = System::MakeObject<Aspose::Words::Bibliography::Person>(u"Roxanne", u"Brielle", u"Tejeda_updated");
// Yeni kişiyi koleksiyona ekle.
persons->Add(person);
ASSERT_EQ(1, persons->get_Count());
// Kişi koleksiyonda varsa kaldır.
if (persons->Contains(person))
{
    persons->Remove(person);
}
ASSERT_EQ(0, persons->get_Count());

// İki kişi içeren bir kişi koleksiyonu oluştur.
persons = System::MakeObject<Aspose::Words::Bibliography::PersonCollection>(System::MakeArray<System::SharedPtr<Aspose::Words::Bibliography::Person>>({System::MakeObject<Aspose::Words::Bibliography::Person>(u"Roxanne_1", u"Brielle_1", u"Tejeda_1"), System::MakeObject<Aspose::Words::Bibliography::Person>(u"Roxanne_2", u"Brielle_2", u"Tejeda_2")}));
ASSERT_EQ(2, persons->get_Count());
// Koleksiyondan kişiyi indeksine göre kaldır.
persons->RemoveAt(0);
ASSERT_EQ(1, persons->get_Count());
// Koleksiyondan tüm kişileri kaldır.
persons->Clear();
ASSERT_EQ(0, persons->get_Count());
```

## Ayrıca Bakınız

* Class [PersonCollection](../)
* Namespace [Aspose::Words::Bibliography](../../)
* Library [Aspose.Words for C++](../../../)
## PersonCollection::PersonCollection(const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Bibliography::Person\>\>\&) constructor


Yeni bir [PersonCollection](../) sınıfı örneği oluştur.

```cpp
Aspose::Words::Bibliography::PersonCollection::PersonCollection(const System::ArrayPtr<System::SharedPtr<Aspose::Words::Bibliography::Person>> &persons)
```


## Örnekler



Kişi koleksiyonu ile nasıl çalışılacağını gösterir.
```cpp
// Yeni bir kişi koleksiyonu oluştur.
auto persons = System::MakeObject<Aspose::Words::Bibliography::PersonCollection>();
auto person = System::MakeObject<Aspose::Words::Bibliography::Person>(u"Roxanne", u"Brielle", u"Tejeda_updated");
// Yeni kişiyi koleksiyona ekle.
persons->Add(person);
ASSERT_EQ(1, persons->get_Count());
// Kişi koleksiyonda varsa kaldır.
if (persons->Contains(person))
{
    persons->Remove(person);
}
ASSERT_EQ(0, persons->get_Count());

// İki kişi içeren bir kişi koleksiyonu oluştur.
persons = System::MakeObject<Aspose::Words::Bibliography::PersonCollection>(System::MakeArray<System::SharedPtr<Aspose::Words::Bibliography::Person>>({System::MakeObject<Aspose::Words::Bibliography::Person>(u"Roxanne_1", u"Brielle_1", u"Tejeda_1"), System::MakeObject<Aspose::Words::Bibliography::Person>(u"Roxanne_2", u"Brielle_2", u"Tejeda_2")}));
ASSERT_EQ(2, persons->get_Count());
// Koleksiyondan kişiyi indeksine göre kaldır.
persons->RemoveAt(0);
ASSERT_EQ(1, persons->get_Count());
// Koleksiyondan tüm kişileri kaldır.
persons->Clear();
ASSERT_EQ(0, persons->get_Count());
```

## Ayrıca Bakınız

* Class [Person](../../person/)
* Class [PersonCollection](../)
* Namespace [Aspose::Words::Bibliography](../../)
* Library [Aspose.Words for C++](../../../)
## PersonCollection::PersonCollection(const System::SharedPtr\<System::Collections::Generic::IEnumerable\<System::SharedPtr\<Aspose::Words::Bibliography::Person\>\>\>\&) constructor




```cpp
Aspose::Words::Bibliography::PersonCollection::PersonCollection(const System::SharedPtr<System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Bibliography::Person>>> &persons)
```

## Ayrıca Bakınız

* Class [Person](../../person/)
* Class [PersonCollection](../)
* Namespace [Aspose::Words::Bibliography](../../)
* Library [Aspose.Words for C++](../../../)
