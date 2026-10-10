---
title: "Aspose::Words::Vba::VbaModuleCollection::get_Count yöntemi"
linktitle: "get_Count"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Vba::VbaModuleCollection::get_Count yöntemi. C++'ta koleksiyondaki VBA modüllerinin sayısını döndürür."
type: docs
weight: 7000
url: /tr/cpp/aspose.words.vba/vbamodulecollection/get_count/
---
## VbaModuleCollection::get_Count method


Koleksiyondaki VBA modüllerinin sayısını döndürür.

```cpp
int32_t Aspose::Words::Vba::VbaModuleCollection::get_Count()
```


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

* Class [VbaModuleCollection](../)
* Namespace [Aspose::Words::Vba](../../)
* Library [Aspose.Words for C++](../../../)
