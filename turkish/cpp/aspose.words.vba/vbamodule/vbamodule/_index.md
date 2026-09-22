---
title: "Aspose::Words::Vba::VbaModule::VbaModule yapıcı"
linktitle: "VbaModule"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Vba::VbaModule::VbaModule yapıcı. C++'ta boş bir modül oluşturur."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.vba/vbamodule/vbamodule/
---
## VbaModule::VbaModule constructor


Boş bir modül oluşturur.

```cpp
Aspose::Words::Vba::VbaModule::VbaModule()
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

* Class [VbaModule](../)
* Namespace [Aspose::Words::Vba](../../)
* Library [Aspose.Words for C++](../../../)
