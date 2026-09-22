---
title: "Aspose::Words::Fields::DropDownItemCollection sınıfı"
linktitle: "DropDownItemCollection"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::DropDownItemCollection sınıfı. Bir açılır form alanındaki tüm öğeleri temsil eden dize koleksiyonu. Daha fazla bilgi edinmek için C++'daki dokümantasyon makalesini ziyaret edin."
type: docs
weight: 4000
url: /tr/cpp/aspose.words.fields/dropdownitemcollection/
---
## DropDownItemCollection class


Açılır form alanındaki tüm öğeleri temsil eden dize koleksiyonu. Daha fazla bilgi için [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) dokümantasyon makalesini ziyaret edin.

```cpp
class DropDownItemCollection : public System::Collections::Generic::IEnumerable<System::String>,
                               public Aspose::Words::IComplexAttr
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [Add](./add/)(const System::String\&) | Koleksiyonun sonuna bir dize ekler. |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Clear](./clear/)() | Koleksiyondaki tüm öğeleri kaldırır. |
| [Contains](./contains/)(const System::String\&) | Koleksiyonun belirtilen değeri içerip içermediğini belirler. |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Koleksiyonda bulunan eleman sayısını alır. |
| [GetEnumerator](./getenumerator/)() override | Koleksiyondaki tüm öğeler üzerinde yineleme yapmak için kullanılabilecek bir enumeratör nesnesi döndürür. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Belirtilen indeksteki öğeyi alır veya ayarlar. |
| [idx_set](./idx_set/)(int32_t, const System::String\&) | Belirtilen indeksteki öğeyi alır veya ayarlar. |
| [IndexOf](./indexof/)(const System::String\&) | Koleksiyondaki belirtilen değerin sıfır tabanlı indeksini döndürür. |
| [Insert](./insert/)(int32_t, const System::String\&) | Belirtilen indekste koleksiyona bir dize ekler. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::String\&) | Belirtilen değeri koleksiyondan kaldırır. |
| [RemoveAt](./removeat/)(int32_t) | Belirtilen indeksteki bir değeri kaldırır. |
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

## Örnekler



Bir combo kutusu alanı eklemeyi ve öğe koleksiyonundaki öğeleri düzenlemeyi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Bir combo kutusu ekleyin ve ardından onun açılır öğe koleksiyonunu doğrulayın.
// Microsoft Word'de kullanıcı combo kutusuna tıklar,
// ve ardından koleksiyondaki metin öğelerinden birini görüntülemek için seçer.
System::ArrayPtr<System::String> items = System::MakeArray<System::String>({u"One", u"Two", u"Three"});
System::SharedPtr<Aspose::Words::Fields::FormField> comboBoxField = builder->InsertComboBox(u"DropDown", items, 0);
System::SharedPtr<Aspose::Words::Fields::DropDownItemCollection> dropDownItems = comboBoxField->get_DropDownItems();

ASSERT_EQ(3, dropDownItems->get_Count());
ASSERT_EQ(u"One", dropDownItems->idx_get(0));
ASSERT_EQ(1, dropDownItems->IndexOf(u"Two"));
ASSERT_TRUE(dropDownItems->Contains(u"Three"));

// Mevcut bir açılır kutu öğeleri koleksiyonuna yeni bir öğe eklemenin iki yolu vardır.
// 1 -  Öğeyi koleksiyonun sonuna ekle:
dropDownItems->Add(u"Four");

// 2 -  Belirtilen indekste başka bir öğenin önüne bir öğe ekle:
dropDownItems->Insert(3, u"Three and a half");

ASSERT_EQ(5, dropDownItems->get_Count());

// Koleksiyon üzerinde yineleme yapın ve her öğeyi yazdırın.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::String>> dropDownCollectionEnumerator = dropDownItems->GetEnumerator();
    while (dropDownCollectionEnumerator->MoveNext())
    {
        std::cout << dropDownCollectionEnumerator->get_Current() << std::endl;
    }
}

// Açılır öğe koleksiyonundan öğeleri kaldırmanın iki yolu vardır.
// 1 -  Geçilen dizeye eşit içeriğe sahip bir öğeyi kaldır:
dropDownItems->Remove(u"Four");

// 2 -  Bir indekste bir öğeyi kaldır:
dropDownItems->RemoveAt(3);

ASSERT_EQ(3, dropDownItems->get_Count());
ASSERT_FALSE(dropDownItems->Contains(u"Three and a half"));
ASSERT_FALSE(dropDownItems->Contains(u"Four"));

doc->Save(get_ArtifactsDir() + u"FormFields.DropDownItemCollection.html");

// Tüm açılır öğe koleksiyonunu boşalt.
dropDownItems->Clear();
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
