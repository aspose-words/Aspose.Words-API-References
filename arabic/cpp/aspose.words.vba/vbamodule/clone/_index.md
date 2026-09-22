---
title: "طريقة Aspose::Words::Vba::VbaModule::Clone"
linktitle: "Clone"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Vba::VbaModule::Clone. تقوم بعمل نسخة من VbaModule في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.vba/vbamodule/clone/
---
## VbaModule::Clone method


يقوم بعمل نسخة من [VbaModule](../).

```cpp
System::SharedPtr<Aspose::Words::Vba::VbaModule> Aspose::Words::Vba::VbaModule::Clone()
```


### ReturnValue

الوحدة المستنسخة [VbaModule](../).

## أمثلة



يظهر كيفية استنساخ عميق لمشروع VBA ووحدة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"VBA project.docm");
auto destDoc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::Vba::VbaProject> copyVbaProject = doc->get_VbaProject()->Clone();
destDoc->set_VbaProject(copyVbaProject);

// في المستند الهدف، لدينا بالفعل وحدة باسم "Module1"
// لأننا استنسخناها مع المشروع. سنحتاج إلى إزالة الوحدة.
System::SharedPtr<Aspose::Words::Vba::VbaModule> oldVbaModule = destDoc->get_VbaProject()->get_Modules()->idx_get(u"Module1");
System::SharedPtr<Aspose::Words::Vba::VbaModule> copyVbaModule = doc->get_VbaProject()->get_Modules()->idx_get(u"Module1")->Clone();
destDoc->get_VbaProject()->get_Modules()->Remove(oldVbaModule);
destDoc->get_VbaProject()->get_Modules()->Add(copyVbaModule);

destDoc->Save(get_ArtifactsDir() + u"VbaProject.CloneVbaProject.docm");
```

## انظر أيضًا

* Class [VbaModule](../)
* Class [VbaModule](../)
* Namespace [Aspose::Words::Vba](../../)
* Library [Aspose.Words for C++](../../../)
