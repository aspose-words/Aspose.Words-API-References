---
title: "Aspose::Words::Vba::VbaModule::get_Type yöntemi"
linktitle: "get_Type"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Vba::VbaModule::get_Type yöntemi. Modülün prosedürel modül, belge modülü, sınıf modülü veya tasarımcı modülü olup olmadığını C++'ta belirtir."
type: docs
weight: 6000
url: /tr/cpp/aspose.words.vba/vbamodule/get_type/
---
## VbaModule::get_Type method


Modülün prosedür modülü, belge modülü, sınıf modülü veya tasarımcı modülü olup olmadığını belirtir.

```cpp
Aspose::Words::Vba::VbaModuleType Aspose::Words::Vba::VbaModule::get_Type() const
```


## Örnekler



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

* Enum [VbaModuleType](../../vbamoduletype/)
* Class [VbaModule](../)
* Namespace [Aspose::Words::Vba](../../)
* Library [Aspose.Words for C++](../../../)
