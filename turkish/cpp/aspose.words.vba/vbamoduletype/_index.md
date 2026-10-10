---
title: "Aspose::Words::Vba::VbaModuleType enum"
linktitle: "VbaModuleType"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Vba::VbaModuleType enum. C++'da bir VBA projesindeki modelin türünü belirtir."
type: docs
weight: 6000
url: /tr/cpp/aspose.words.vba/vbamoduletype/
---
## VbaModuleType enum


Bir VBA projesindeki modelin tipini belirtir.

```cpp
enum class VbaModuleType
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| DocumentModule | 0 | Bir belgeyle ilişkili gömülü makrolar ve programatik erişim işlemleri için bir modül belirten VBA proje öğesi türüdür. |
| ProceduralModule | 1 | Alt yordamlar ve işlevlerden oluşan bir koleksiyon. |
| ClassModule | 2 | Yeni bir nesnenin tanımını içeren bir modül. Bir sınıfın her örneği yeni bir nesne oluşturur ve modülde tanımlanan prosedürler nesnenin özellikleri ve yöntemleri haline gelir. |
| DesignerModule | 3 | Projeye kaydedilmiş bir ActiveX denetiminin yöntem ve özelliklerini genişleten bir VBA modülü. |


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

* Namespace [Aspose::Words::Vba](../)
* Library [Aspose.Words for C++](../../)
