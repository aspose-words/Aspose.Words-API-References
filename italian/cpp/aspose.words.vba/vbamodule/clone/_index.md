---
title: "Aspose::Words::Vba::VbaModule::Clone metodo"
linktitle: "Clone"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Vba::VbaModule::Clone. Esegue una copia del VbaModule in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.vba/vbamodule/clone/
---
## VbaModule::Clone method


Esegue una copia del [VbaModule](../).

```cpp
System::SharedPtr<Aspose::Words::Vba::VbaModule> Aspose::Words::Vba::VbaModule::Clone()
```


### ReturnValue

Il [VbaModule](../) clonato.

## Esempi



Mostra come clonare in profondità un progetto VBA e un modulo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"VBA project.docm");
auto destDoc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::Vba::VbaProject> copyVbaProject = doc->get_VbaProject()->Clone();
destDoc->set_VbaProject(copyVbaProject);

// Nel documento di destinazione, abbiamo già un modulo chiamato "Module1"
// poiché lo abbiamo clonato insieme al progetto. Dovremo rimuovere il modulo.
System::SharedPtr<Aspose::Words::Vba::VbaModule> oldVbaModule = destDoc->get_VbaProject()->get_Modules()->idx_get(u"Module1");
System::SharedPtr<Aspose::Words::Vba::VbaModule> copyVbaModule = doc->get_VbaProject()->get_Modules()->idx_get(u"Module1")->Clone();
destDoc->get_VbaProject()->get_Modules()->Remove(oldVbaModule);
destDoc->get_VbaProject()->get_Modules()->Add(copyVbaModule);

destDoc->Save(get_ArtifactsDir() + u"VbaProject.CloneVbaProject.docm");
```

## Vedi anche

* Class [VbaModule](../)
* Class [VbaModule](../)
* Namespace [Aspose::Words::Vba](../../)
* Library [Aspose.Words for C++](../../../)
