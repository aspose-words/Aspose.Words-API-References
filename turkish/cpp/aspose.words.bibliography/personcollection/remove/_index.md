---
title: "Aspose::Words::Bibliography::PersonCollection::Remove metodu"
linktitle: "Remove"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Bibliography::PersonCollection::Remove metodu. Kişiyi koleksiyondan C++'ta kaldırır."
type: docs
weight: 11000
url: /tr/cpp/aspose.words.bibliography/personcollection/remove/
---
## PersonCollection::Remove method


Kişiyi koleksiyondan kaldırır.

```cpp
bool Aspose::Words::Bibliography::PersonCollection::Remove(const System::SharedPtr<Aspose::Words::Bibliography::Person> &person)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| kişi | const System::SharedPtr\<Aspose::Words::Bibliography::Person\>\& | Koleksiyondan kaldırılacak kişi. |

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
