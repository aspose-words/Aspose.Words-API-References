---
title: "Aspose::Words::Fields::DropDownItemCollection::RemoveAt metodu"
linktitle: "RemoveAt"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::DropDownItemCollection::RemoveAt metodu. Belirtilen indeksteki bir değeri C++'ta kaldırır."
type: docs
weight: 18000
url: /tr/cpp/aspose.words.fields/dropdownitemcollection/removeat/
---
## DropDownItemCollection::RemoveAt method


Belirtilen indeksteki bir değeri kaldırır.

```cpp
void Aspose::Words::Fields::DropDownItemCollection::RemoveAt(int32_t index)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| index | int32_t | Sıfır tabanlı indeks. |

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

* Class [DropDownItemCollection](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
