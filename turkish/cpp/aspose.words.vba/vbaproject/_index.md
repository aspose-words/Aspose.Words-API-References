---
title: "Aspose::Words::Vba::VbaProject class"
linktitle: "VbaProject"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Vba::VbaProject sınıfı. VBA proje bilgilerine erişim sağlar. Belgede bulunan bir VBA projesi, VBA modüllerinin bir koleksiyonu olarak tanımlanır. Daha fazla bilgi için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.vba/vbaproject/
---
## VbaProject class


VBA proje bilgilerine erişim sağlar. Belgedeki bir VBA projesi, VBA modüllerinin bir koleksiyonu olarak tanımlanır. Daha fazla bilgi için, [Working with VBA Macros](https://docs.aspose.com/words/cpp/working-with-vba-macros/) dokümantasyon makalesini ziyaret edin.

```cpp
class VbaProject : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [Clone](./clone/)() | [VbaProject](./) öğesinin bir kopyasını oluşturur. |
| [get_CodePage](./get_codepage/)() const | VBA projesinin kod sayfasını alır veya ayarlar. |
| [get_IsProtected](./get_isprotected/)() | [VbaProject](./) öğesinin şifre korumalı olup olmadığını gösterir. |
| [get_IsSigned](./get_issigned/)() | [VbaProject](./) öğesinin imzalı olup olmadığını gösterir. |
| [get_Modules](./get_modules/)() | VBA proje modüllerinin koleksiyonunu döndürür. |
| [get_Name](./get_name/)() const | VBA projesinin adını alır veya ayarlar. |
| [get_References](./get_references/)() | VBA proje referanslarının bir koleksiyonunu alır. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_CodePage](./set_codepage/)(int32_t) | [Aspose::Words::Vba::VbaProject::get_CodePage](./get_codepage/) için ayarlayıcı. |
| [set_Name](./set_name/)(const System::String\&) | [Aspose::Words::Vba::VbaProject::get_Name](./get_name/) için ayarlayıcı. |
| static [Type](./type/)() |  |
| [VbaProject](./vbaproject/)() | Boş bir [VbaProject](./) oluşturur. |

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
