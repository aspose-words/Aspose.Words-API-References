---
title: "Aspose::Words::Vba::VbaModule::Clone metodu"
linktitle: "Clone"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Vba::VbaModule::Clone yöntemi. C++'ta VbaModule'un bir kopyasını oluşturur."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.vba/vbamodule/clone/
---
## VbaModule::Clone method


[VbaModule](../) kopyasını oluşturur.

```cpp
System::SharedPtr<Aspose::Words::Vba::VbaModule> Aspose::Words::Vba::VbaModule::Clone()
```


### ReturnValue

Klonlanmış [VbaModule](../).

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

* Class [VbaModule](../)
* Class [VbaModule](../)
* Namespace [Aspose::Words::Vba](../../)
* Library [Aspose.Words for C++](../../../)
