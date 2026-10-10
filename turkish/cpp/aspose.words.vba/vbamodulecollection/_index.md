---
title: "Aspose::Words::Vba::VbaModuleCollection class"
linktitle: "VbaModuleCollection"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Vba::VbaModuleCollection sınıfı. VbaModule nesnelerinin bir koleksiyonunu temsil eder. Daha fazla bilgi için C++ belgeleri makalesini ziyaret edin."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.vba/vbamodulecollection/
---
## VbaModuleCollection class


VbaModule nesnelerinin bir koleksiyonunu temsil eder. Daha fazla bilgi için [Working with VBA Macros](https://docs.aspose.com/words/cpp/working-with-vba-macros/) belgeleri makalesini ziyaret edin.

```cpp
class VbaModuleCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Vba::VbaModule>>
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::Vba::VbaModule\>\&) | Koleksiyona bir modül ekler. |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Koleksiyondaki VBA modüllerinin sayısını döndürür. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | İndeks ile bir [VbaModule](../vbamodule/) nesnesi alır. |
| [idx_get](./idx_get/)(const System::String\&) | İsim ile bir [VbaModule](../vbamodule/) nesnesi alır, bulunamazsa Null döner. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::SharedPtr\<Aspose::Words::Vba::VbaModule\>\&) | Belirtilen modülü koleksiyondan kaldırır. |
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



Bir belgenin VBA proje bilgilerine nasıl erişileceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"VBA project.docm");

// Bir VBA projesi, VBA modüllerinden oluşan bir koleksiyon içerir.
System::SharedPtr<Aspose::Words::Vba::VbaProject> vbaProject = doc->get_VbaProject();
std::cout << (vbaProject->get_IsSigned() ? System::String::Format(u"Project name: {0} signed; Project code page: {1}; Modules count: {2}\n", vbaProject->get_Name(), vbaProject->get_CodePage(), vbaProject->get_Modules()->LINQ_Count()) : System::String::Format(u"Project name: {0} not signed; Project code page: {1}; Modules count: {2}\n", vbaProject->get_Name(), vbaProject->get_CodePage(), vbaProject->get_Modules()->LINQ_Count())) << std::endl;

System::SharedPtr<Aspose::Words::Vba::VbaModuleCollection> vbaModules = doc->get_VbaProject()->get_Modules();

ASSERT_EQ(vbaModules->LINQ_Count(), 3);

for (auto&& module_ : vbaModules)
{
    std::cout << System::String::Format(u"Module name: {0};\nModule code:\n{1}\n", module_->get_Name(), module_->get_SourceCode()) << std::endl;
}

// VBA modülü için yeni kaynak kodunu ayarlayın. Koleksiyondaki VBA modüllerine indeks ya da ad ile erişebilirsiniz.
vbaModules->idx_get(0)->set_SourceCode(u"Your VBA code...");
vbaModules->idx_get(u"Module1")->set_SourceCode(u"Your VBA code...");

// Bir modülü koleksiyondan kaldırın.
vbaModules->Remove(vbaModules->idx_get(2));
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Vba](../)
* Library [Aspose.Words for C++](../../)
