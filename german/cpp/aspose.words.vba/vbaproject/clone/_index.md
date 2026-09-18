---
title: "Aspose::Words::Vba::VbaProject::Clone Methode"
linktitle: "Klonen"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Vba::VbaProject::Clone Methode. Führt eine Kopie des VbaProject in C++ aus."
type: docs
weight: 3000
url: /de/cpp/aspose.words.vba/vbaproject/clone/
---
## VbaProject::Clone method


Führt eine Kopie des [VbaProject](../) aus.

```cpp
System::SharedPtr<Aspose::Words::Vba::VbaProject> Aspose::Words::Vba::VbaProject::Clone()
```


### ReturnValue

Das geklonte [VbaProject](../).

## Beispiele



Zeigt, wie man ein VBA-Projekt und -Modul tief klont.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"VBA project.docm");
auto destDoc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::Vba::VbaProject> copyVbaProject = doc->get_VbaProject()->Clone();
destDoc->set_VbaProject(copyVbaProject);

// Im Zieldokument haben wir bereits ein Modul mit dem Namen "Module1"
// weil wir es zusammen mit dem Projekt geklont haben. Wir müssen das Modul entfernen.
System::SharedPtr<Aspose::Words::Vba::VbaModule> oldVbaModule = destDoc->get_VbaProject()->get_Modules()->idx_get(u"Module1");
System::SharedPtr<Aspose::Words::Vba::VbaModule> copyVbaModule = doc->get_VbaProject()->get_Modules()->idx_get(u"Module1")->Clone();
destDoc->get_VbaProject()->get_Modules()->Remove(oldVbaModule);
destDoc->get_VbaProject()->get_Modules()->Add(copyVbaModule);

destDoc->Save(get_ArtifactsDir() + u"VbaProject.CloneVbaProject.docm");
```

## Siehe auch

* Class [VbaProject](../)
* Class [VbaProject](../)
* Namespace [Aspose::Words::Vba](../../)
* Library [Aspose.Words for C++](../../../)
