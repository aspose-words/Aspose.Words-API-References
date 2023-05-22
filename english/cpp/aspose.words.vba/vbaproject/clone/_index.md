---
title: Aspose::Words::Vba::VbaProject::Clone method
linktitle: Clone
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Vba::VbaProject::Clone method. Performs a copy of the VbaProject in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words.vba/vbaproject/clone/
---
## VbaProject::Clone method


Performs a copy of the [VbaProject](../).

```cpp
System::SharedPtr<Aspose::Words::Vba::VbaProject> Aspose::Words::Vba::VbaProject::Clone()
```


### ReturnValue

The cloned [VbaProject](../).

## Examples



Shows how to deep clone a VBA project and module. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"VBA project.docm");
auto destDoc = MakeObject<Document>();

SharedPtr<VbaProject> copyVbaProject = doc->get_VbaProject()->Clone();
destDoc->set_VbaProject(copyVbaProject);

// In the destination document, we already have a module named "Module1"
// because we cloned it along with the project. We will need to remove the module.
SharedPtr<VbaModule> oldVbaModule = destDoc->get_VbaProject()->get_Modules()->idx_get(u"Module1");
SharedPtr<VbaModule> copyVbaModule = doc->get_VbaProject()->get_Modules()->idx_get(u"Module1")->Clone();
destDoc->get_VbaProject()->get_Modules()->Remove(oldVbaModule);
destDoc->get_VbaProject()->get_Modules()->Add(copyVbaModule);

destDoc->Save(ArtifactsDir + u"VbaProject.CloneVbaProject.docm");
```

## See Also

* Class [VbaProject](../)
* Class [VbaProject](../)
* Namespace [Aspose::Words::Vba](../../)
* Library [Aspose.Words for C++](../../../)
