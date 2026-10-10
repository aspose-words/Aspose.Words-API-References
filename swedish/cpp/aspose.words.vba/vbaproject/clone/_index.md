---
title: "Aspose::Words::Vba::VbaProject::Clone metod"
linktitle: "Klona"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Vba::VbaProject::Clone metod. Utför en kopia av VbaProject i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words.vba/vbaproject/clone/
---
## VbaProject::Clone method


Utför en kopia av [VbaProject](../).

```cpp
System::SharedPtr<Aspose::Words::Vba::VbaProject> Aspose::Words::Vba::VbaProject::Clone()
```


### ReturnValue

Den klonade [VbaProject](../).

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

* Class [VbaProject](../)
* Class [VbaProject](../)
* Namespace [Aspose::Words::Vba](../../)
* Library [Aspose.Words for C++](../../../)
