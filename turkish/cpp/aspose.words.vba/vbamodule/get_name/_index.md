---
title: "Aspose::Words::Vba::VbaModule::get_Name metodu"
linktitle: "get_Name"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Vba::VbaModule::get_Name metodu. VBA proje modülü adını alır veya ayarlar C++'ta."
type: docs
weight: 4000
url: /tr/cpp/aspose.words.vba/vbamodule/get_name/
---
## VbaModule::get_Name method


VBA proje modülünün adını alır veya ayarlar.

```cpp
System::String Aspose::Words::Vba::VbaModule::get_Name() const
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


Makrolar kullanarak bir VBA projesi oluşturmayı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Yeni bir VBA projesi oluştur.
auto project = System::MakeObject<Aspose::Words::Vba::VbaProject>();
project->set_Name(u"Aspose.Project");
doc->set_VbaProject(project);

// Yeni bir modül oluştur ve bir makro kaynak kodu belirt.
auto module_ = System::MakeObject<Aspose::Words::Vba::VbaModule>();
module_->set_Name(u"Aspose.Module");
module_->set_Type(Aspose::Words::Vba::VbaModuleType::ProceduralModule);
module_->set_SourceCode(u"New source code");

// Modülü VBA projesine ekle.
doc->get_VbaProject()->get_Modules()->Add(module_);

doc->Save(get_ArtifactsDir() + u"VbaProject.CreateVBAMacros.docm");
```

## Ayrıca Bakınız

* Class [VbaModule](../)
* Namespace [Aspose::Words::Vba](../../)
* Library [Aspose.Words for C++](../../../)
