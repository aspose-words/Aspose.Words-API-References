---
title: "Aspose::Words::Vba::VbaModule class"
linktitle: "VbaModule"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Vba::VbaModule sınıfı. VBA proje modülüne erişim sağlar. Daha fazla bilgi için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 1000
url: /tr/cpp/aspose.words.vba/vbamodule/
---
## VbaModule class


VBA proje modülüne erişim sağlar. Daha fazla bilgi için, [Working with VBA Macros](https://docs.aspose.com/words/cpp/working-with-vba-macros/) dokümantasyon makalesini ziyaret edin.

```cpp
class VbaModule : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [Clone](./clone/)() | [VbaModule](./) öğesinin bir kopyasını gerçekleştirir. |
| [get_Name](./get_name/)() const | VBA proje modülünün adını alır veya ayarlar. |
| [get_SourceCode](./get_sourcecode/)() const | VBA proje modülünün kaynak kodunu alır veya ayarlar. |
| [get_Type](./get_type/)() const | Modülün prosedür modülü, belge modülü, sınıf modülü veya tasarımcı modülü olup olmadığını belirtir. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Name](./set_name/)(const System::String\&) | [Aspose::Words::Vba::VbaModule::get_Name](./get_name/) için ayarlayıcı. |
| [set_SourceCode](./set_sourcecode/)(const System::String\&) | [Aspose::Words::Vba::VbaModule::get_SourceCode](./get_sourcecode/) için ayarlayıcı. |
| [set_Type](./set_type/)(Aspose::Words::Vba::VbaModuleType) | [Aspose::Words::Vba::VbaModule::get_Type](./get_type/) için ayarlayıcı. |
| static [Type](./type/)() |  |
| [VbaModule](./vbamodule/)() | Boş bir modül oluşturur. |

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
