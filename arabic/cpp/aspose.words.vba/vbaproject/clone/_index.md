---
title: "طريقة Aspose::Words::Vba::VbaProject::Clone"
linktitle: "Clone"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Vba::VbaProject::Clone. تقوم بإنشاء نسخة من VbaProject في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.vba/vbaproject/clone/
---
## VbaProject::Clone method


يقوم بإنشاء نسخة من [VbaProject](../).

```cpp
System::SharedPtr<Aspose::Words::Vba::VbaProject> Aspose::Words::Vba::VbaProject::Clone()
```


### ReturnValue

[VbaProject](../) المستنسخ.

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

* Class [VbaProject](../)
* Class [VbaProject](../)
* Namespace [Aspose::Words::Vba](../../)
* Library [Aspose.Words for C++](../../../)
