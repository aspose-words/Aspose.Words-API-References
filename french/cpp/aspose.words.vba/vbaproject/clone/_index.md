---
title: "Aspose::Words::Vba::VbaProject::Clone méthode"
linktitle: "Clone"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Vba::VbaProject::Clone méthode. Effectue une copie du VbaProject en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words.vba/vbaproject/clone/
---
## VbaProject::Clone method


Effectue une copie du [VbaProject](../).

```cpp
System::SharedPtr<Aspose::Words::Vba::VbaProject> Aspose::Words::Vba::VbaProject::Clone()
```


### ReturnValue

Le [VbaProject](../) cloné.

## Exemples



Montre comment dupliquer en profondeur un projet VBA et un module.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"VBA project.docm");
auto destDoc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::Vba::VbaProject> copyVbaProject = doc->get_VbaProject()->Clone();
destDoc->set_VbaProject(copyVbaProject);

// Dans le document de destination, nous avons déjà un module nommé "Module1"
// car nous l'avons cloné avec le projet. Nous devrons supprimer le module.
System::SharedPtr<Aspose::Words::Vba::VbaModule> oldVbaModule = destDoc->get_VbaProject()->get_Modules()->idx_get(u"Module1");
System::SharedPtr<Aspose::Words::Vba::VbaModule> copyVbaModule = doc->get_VbaProject()->get_Modules()->idx_get(u"Module1")->Clone();
destDoc->get_VbaProject()->get_Modules()->Remove(oldVbaModule);
destDoc->get_VbaProject()->get_Modules()->Add(copyVbaModule);

destDoc->Save(get_ArtifactsDir() + u"VbaProject.CloneVbaProject.docm");
```

## Voir aussi

* Class [VbaProject](../)
* Class [VbaProject](../)
* Namespace [Aspose::Words::Vba](../../)
* Library [Aspose.Words for C++](../../../)
