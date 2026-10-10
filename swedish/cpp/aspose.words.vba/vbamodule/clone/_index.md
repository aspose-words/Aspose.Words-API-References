---
title: "Aspose::Words::Vba::VbaModule::Clone-metod"
linktitle: "Klona"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Vba::VbaModule::Clone-metod. Utför en kopia av VbaModule i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words.vba/vbamodule/clone/
---
## VbaModule::Clone method


Utför en kopia av [VbaModule](../).

```cpp
System::SharedPtr<Aspose::Words::Vba::VbaModule> Aspose::Words::Vba::VbaModule::Clone()
```


### ReturnValue

Den klonade [VbaModule](../).

## Exempel



Visar hur man djupklonar ett VBA-projekt och en modul.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"VBA project.docm");
auto destDoc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::Vba::VbaProject> copyVbaProject = doc->get_VbaProject()->Clone();
destDoc->set_VbaProject(copyVbaProject);

// I destinationsdokumentet har vi redan en modul med namnet "Module1"
// eftersom vi klonade den tillsammans med projektet. Vi måste ta bort modulen.
System::SharedPtr<Aspose::Words::Vba::VbaModule> oldVbaModule = destDoc->get_VbaProject()->get_Modules()->idx_get(u"Module1");
System::SharedPtr<Aspose::Words::Vba::VbaModule> copyVbaModule = doc->get_VbaProject()->get_Modules()->idx_get(u"Module1")->Clone();
destDoc->get_VbaProject()->get_Modules()->Remove(oldVbaModule);
destDoc->get_VbaProject()->get_Modules()->Add(copyVbaModule);

destDoc->Save(get_ArtifactsDir() + u"VbaProject.CloneVbaProject.docm");
```

## Se även

* Class [VbaModule](../)
* Class [VbaModule](../)
* Namespace [Aspose::Words::Vba](../../)
* Library [Aspose.Words for C++](../../../)
