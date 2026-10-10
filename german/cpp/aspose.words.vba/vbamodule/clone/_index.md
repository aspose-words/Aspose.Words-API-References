---
title: "Aspose::Words::Vba::VbaModule::Clone Methode"
linktitle: "Klonen"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Vba::VbaModule::Clone Methode. Führt eine Kopie des VbaModule in C++ aus."
type: docs
weight: 3000
url: /de/cpp/aspose.words.vba/vbamodule/clone/
---
## VbaModule::Clone method


Führt eine Kopie des [VbaModule](../) aus.

```cpp
System::SharedPtr<Aspose::Words::Vba::VbaModule> Aspose::Words::Vba::VbaModule::Clone()
```


### ReturnValue

Das geklonte [VbaModule](../).

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

* Class [VbaModule](../)
* Class [VbaModule](../)
* Namespace [Aspose::Words::Vba](../../)
* Library [Aspose.Words for C++](../../../)
