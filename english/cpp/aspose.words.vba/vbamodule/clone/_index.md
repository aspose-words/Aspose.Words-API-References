---
title: Aspose::Words::Vba::VbaModule::Clone method
linktitle: Clone
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Vba::VbaModule::Clone method. Performs a copy of the VbaModule in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words.vba/vbamodule/clone/
---
## VbaModule::Clone method


Performs a copy of the [VbaModule](../).

```cpp
System::SharedPtr<Aspose::Words::Vba::VbaModule> Aspose::Words::Vba::VbaModule::Clone()
```


### ReturnValue

The cloned [VbaModule](../).

## Examples



Shows how to deep clone a VBA project and module. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"VBA project.docm");
auto destDoc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::Vba::VbaProject> copyVbaProject = doc->get_VbaProject()->Clone();
destDoc->set_VbaProject(copyVbaProject);

// In the destination document, we already have a module named "Module1"
// because we cloned it along with the project. We will need to remove the module.
System::SharedPtr<Aspose::Words::Vba::VbaModule> oldVbaModule = destDoc->get_VbaProject()->get_Modules()->idx_get(u"Module1");
System::SharedPtr<Aspose::Words::Vba::VbaModule> copyVbaModule = doc->get_VbaProject()->get_Modules()->idx_get(u"Module1")->Clone();
destDoc->get_VbaProject()->get_Modules()->Remove(oldVbaModule);
destDoc->get_VbaProject()->get_Modules()->Add(copyVbaModule);

destDoc->Save(get_ArtifactsDir() + u"VbaProject.CloneVbaProject.docm");
```

## See Also

* Class [VbaModule](../)
* Class [VbaModule](../)
* Namespace [Aspose::Words::Vba](../../)
* Library [Aspose.Words for C++](../../../)
