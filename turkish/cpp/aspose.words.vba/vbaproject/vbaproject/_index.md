---
title: "Aspose::Words::Vba::VbaProject::VbaProject yapıcı"
linktitle: "VbaProject"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Vba::VbaProject::VbaProject yapıcı. C++'da boş bir VbaProject oluşturur."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.vba/vbaproject/vbaproject/
---
## VbaProject::VbaProject constructor


Boş bir [VbaProject](../) oluşturur.

```cpp
Aspose::Words::Vba::VbaProject::VbaProject()
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

* Class [VbaProject](../)
* Namespace [Aspose::Words::Vba](../../)
* Library [Aspose.Words for C++](../../../)
