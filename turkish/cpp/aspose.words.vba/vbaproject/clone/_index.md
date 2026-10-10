---
title: "Aspose::Words::Vba::VbaProject::Clone yöntemi"
linktitle: "Clone"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Vba::VbaProject::Clone yöntemi. C++'ta VbaProject'in bir kopyasını oluşturur."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.vba/vbaproject/clone/
---
## VbaProject::Clone method


[VbaProject](../) öğesinin bir kopyasını oluşturur.

```cpp
System::SharedPtr<Aspose::Words::Vba::VbaProject> Aspose::Words::Vba::VbaProject::Clone()
```


### ReturnValue

Klonlanmış [VbaProject](../).

## Örnekler



Bir VBA projesi ve modülünün derin klonlanmasını nasıl yapacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"VBA project.docm");
auto destDoc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::Vba::VbaProject> copyVbaProject = doc->get_VbaProject()->Clone();
destDoc->set_VbaProject(copyVbaProject);

// Hedef belgede, zaten "Module1" adlı bir modülümüz var
// çünkü projeyle birlikte onu klonladık. Modülü kaldırmamız gerekecek.
System::SharedPtr<Aspose::Words::Vba::VbaModule> oldVbaModule = destDoc->get_VbaProject()->get_Modules()->idx_get(u"Module1");
System::SharedPtr<Aspose::Words::Vba::VbaModule> copyVbaModule = doc->get_VbaProject()->get_Modules()->idx_get(u"Module1")->Clone();
destDoc->get_VbaProject()->get_Modules()->Remove(oldVbaModule);
destDoc->get_VbaProject()->get_Modules()->Add(copyVbaModule);

destDoc->Save(get_ArtifactsDir() + u"VbaProject.CloneVbaProject.docm");
```

## Ayrıca Bakınız

* Class [VbaProject](../)
* Class [VbaProject](../)
* Namespace [Aspose::Words::Vba](../../)
* Library [Aspose.Words for C++](../../../)
