---
title: "Aspose::Words::VariableCollection::idx_get yöntemi"
linktitle: "idx_get"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::VariableCollection::idx_get yöntemi. Büyük/küçük harfe duyarsız isimle bir belge değişkenini alır veya ayarlar. Atamanın sağ tarafında null değerlerine izin verilmez ve C++'ta boş string ile değiştirilir."
type: docs
weight: 12000
url: /tr/cpp/aspose.words/variablecollection/idx_get/
---
## VariableCollection::idx_get(const System::String\&) method


Büyük/küçük harfe duyarsız adla bir belge değişkenini alır veya ayarlar. **null** değerleri atamanın sağ tarafı olarak izin verilmez ve boş string ile değiştirilir.

```cpp
System::String Aspose::Words::VariableCollection::idx_get(const System::String &name)
```


## Örnekler



Bir belgenin değişken koleksiyonu ile nasıl çalışılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::VariableCollection> variables = doc->get_Variables();

// Her belgenin ekleyebileceğimiz anahtar/değer çifti değişkenlerinden oluşan bir koleksiyonu vardır.
variables->Add(u"Home address", u"123 Main St.");
variables->Add(u"City", u"London");
variables->Add(u"Bedrooms", u"3");

ASSERT_EQ(3, variables->get_Count());

// Değişkenlerin değerlerini belge gövdesinde DOCVARIABLE alanlarıyla görüntüleyebiliriz.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldDocVariable>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDocVariable, true));
field->set_VariableName(u"Home address");
field->Update();

ASSERT_EQ(u"123 Main St.", field->get_Result());

// Mevcut anahtarlara değer atamak onları güncelleyecektir.
variables->Add(u"Home address", u"456 Queen St.");

// DOCVARIABLE alanlarını güncelleyerek değerlerin güncel görüntülenmesini sağlamamız gerekir.
ASSERT_EQ(u"123 Main St.", field->get_Result());

field->Update();

ASSERT_EQ(u"456 Queen St.", field->get_Result());

// Belirli bir ad veya değere sahip belge değişkenlerinin varlığını doğrulayın.
ASSERT_TRUE(variables->Contains(u"City"));
ASSERT_TRUE(variables->LINQ_Any(static_cast<System::Func<System::Collections::Generic::KeyValuePair<System::String, System::String>, bool>>(static_cast<std::function<bool(System::Collections::Generic::KeyValuePair<System::String, System::String> v)>>([](System::Collections::Generic::KeyValuePair<System::String, System::String> v) -> bool
{
    return v.get_Value() == u"London";
}))));

// Değişken koleksiyonu, değişkenleri adlarına göre alfabetik olarak otomatik sıralar.
ASSERT_EQ(0, variables->IndexOfKey(u"Bedrooms"));
ASSERT_EQ(1, variables->IndexOfKey(u"City"));
ASSERT_EQ(2, variables->IndexOfKey(u"Home address"));

ASSERT_EQ(u"3", variables->idx_get(0));
ASSERT_EQ(u"London", variables->idx_get(u"City"));

// Değişken koleksiyonunu yineleyin.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::Collections::Generic::KeyValuePair<System::String, System::String>>> enumerator = doc->get_Variables()->GetEnumerator();
    while (enumerator->MoveNext())
    {
        std::cout << System::String::Format(u"Name: {0}, Value: {1}", enumerator->get_Current().get_Key(), enumerator->get_Current().get_Value()) << std::endl;
    }
}

// Aşağıda bir koleksiyondan belge değişkenlerini kaldırmanın üç yolu verilmiştir.
// 1 -  Ada göre:
variables->Remove(u"City");

ASSERT_FALSE(variables->Contains(u"City"));

// 2 -  İndexe göre:
variables->RemoveAt(1);

ASSERT_FALSE(variables->Contains(u"Home address"));

// 3 -  Tüm koleksiyonu bir kerede temizle:
variables->Clear();

ASSERT_EQ(0, variables->get_Count());
```

## Ayrıca Bakınız

* Class [VariableCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## VariableCollection::idx_get(int32_t) method


Belirtilen indeksteki bir belge değişkenini alır veya ayarlar. **null** değerleri atamanın sağ tarafı olarak izin verilmez ve boş string ile değiştirilir.

```cpp
System::String Aspose::Words::VariableCollection::idx_get(int32_t index)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| index | int32_t | Belge değişkeninin sıfır tabanlı indeksi. |

## Örnekler



Bir belgenin değişken koleksiyonu ile nasıl çalışılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::VariableCollection> variables = doc->get_Variables();

// Her belgenin ekleyebileceğimiz anahtar/değer çifti değişkenlerinden oluşan bir koleksiyonu vardır.
variables->Add(u"Home address", u"123 Main St.");
variables->Add(u"City", u"London");
variables->Add(u"Bedrooms", u"3");

ASSERT_EQ(3, variables->get_Count());

// Değişkenlerin değerlerini belge gövdesinde DOCVARIABLE alanlarıyla görüntüleyebiliriz.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldDocVariable>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDocVariable, true));
field->set_VariableName(u"Home address");
field->Update();

ASSERT_EQ(u"123 Main St.", field->get_Result());

// Mevcut anahtarlara değer atamak onları güncelleyecektir.
variables->Add(u"Home address", u"456 Queen St.");

// DOCVARIABLE alanlarını güncelleyerek değerlerin güncel görüntülenmesini sağlamamız gerekir.
ASSERT_EQ(u"123 Main St.", field->get_Result());

field->Update();

ASSERT_EQ(u"456 Queen St.", field->get_Result());

// Belirli bir ad veya değere sahip belge değişkenlerinin varlığını doğrulayın.
ASSERT_TRUE(variables->Contains(u"City"));
ASSERT_TRUE(variables->LINQ_Any(static_cast<System::Func<System::Collections::Generic::KeyValuePair<System::String, System::String>, bool>>(static_cast<std::function<bool(System::Collections::Generic::KeyValuePair<System::String, System::String> v)>>([](System::Collections::Generic::KeyValuePair<System::String, System::String> v) -> bool
{
    return v.get_Value() == u"London";
}))));

// Değişken koleksiyonu, değişkenleri adlarına göre alfabetik olarak otomatik sıralar.
ASSERT_EQ(0, variables->IndexOfKey(u"Bedrooms"));
ASSERT_EQ(1, variables->IndexOfKey(u"City"));
ASSERT_EQ(2, variables->IndexOfKey(u"Home address"));

ASSERT_EQ(u"3", variables->idx_get(0));
ASSERT_EQ(u"London", variables->idx_get(u"City"));

// Değişken koleksiyonunu yineleyin.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::Collections::Generic::KeyValuePair<System::String, System::String>>> enumerator = doc->get_Variables()->GetEnumerator();
    while (enumerator->MoveNext())
    {
        std::cout << System::String::Format(u"Name: {0}, Value: {1}", enumerator->get_Current().get_Key(), enumerator->get_Current().get_Value()) << std::endl;
    }
}

// Aşağıda bir koleksiyondan belge değişkenlerini kaldırmanın üç yolu verilmiştir.
// 1 -  Ada göre:
variables->Remove(u"City");

ASSERT_FALSE(variables->Contains(u"City"));

// 2 -  İndexe göre:
variables->RemoveAt(1);

ASSERT_FALSE(variables->Contains(u"Home address"));

// 3 -  Tüm koleksiyonu bir kerede temizle:
variables->Clear();

ASSERT_EQ(0, variables->get_Count());
```

## Ayrıca Bakınız

* Class [VariableCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
