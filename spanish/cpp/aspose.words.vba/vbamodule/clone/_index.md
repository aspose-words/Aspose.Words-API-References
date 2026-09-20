---
title: "Aspose::Words::Vba::VbaModule::Clone método"
linktitle: "Clonar"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Vba::VbaModule::Clone method. Realiza una copia del VbaModule en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words.vba/vbamodule/clone/
---
## VbaModule::Clone method


Realiza una copia del [VbaModule](../).

```cpp
System::SharedPtr<Aspose::Words::Vba::VbaModule> Aspose::Words::Vba::VbaModule::Clone()
```


### ReturnValue

El [VbaModule](../) clonado.

## Ejemplos



Muestra cómo clonar profundamente un proyecto y módulo VBA.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"VBA project.docm");
auto destDoc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::Vba::VbaProject> copyVbaProject = doc->get_VbaProject()->Clone();
destDoc->set_VbaProject(copyVbaProject);

// En el documento de destino, ya tenemos un módulo llamado "Module1"
// porque lo clonamos junto con el proyecto. Necesitaremos eliminar el módulo.
System::SharedPtr<Aspose::Words::Vba::VbaModule> oldVbaModule = destDoc->get_VbaProject()->get_Modules()->idx_get(u"Module1");
System::SharedPtr<Aspose::Words::Vba::VbaModule> copyVbaModule = doc->get_VbaProject()->get_Modules()->idx_get(u"Module1")->Clone();
destDoc->get_VbaProject()->get_Modules()->Remove(oldVbaModule);
destDoc->get_VbaProject()->get_Modules()->Add(copyVbaModule);

destDoc->Save(get_ArtifactsDir() + u"VbaProject.CloneVbaProject.docm");
```

## Ver también

* Class [VbaModule](../)
* Class [VbaModule](../)
* Namespace [Aspose::Words::Vba](../../)
* Library [Aspose.Words for C++](../../../)
