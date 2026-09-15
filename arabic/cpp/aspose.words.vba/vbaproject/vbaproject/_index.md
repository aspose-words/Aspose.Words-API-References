---
title: "منشئ Aspose::Words::Vba::VbaProject::VbaProject"
linktitle: "VbaProject"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "منشئ Aspose::Words::Vba::VbaProject::VbaProject. ينشئ VbaProject فارغًا في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.vba/vbaproject/vbaproject/
---
## VbaProject::VbaProject constructor


ينشئ [VbaProject](../) فارغًا.

```cpp
Aspose::Words::Vba::VbaProject::VbaProject()
```


## أمثلة



يُظهر كيفية إنشاء مشروع VBA باستخدام الماكرو.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// إنشاء مشروع VBA جديد.
auto project = System::MakeObject<Aspose::Words::Vba::VbaProject>();
project->set_Name(u"Aspose.Project");
doc->set_VbaProject(project);

// إنشاء وحدة جديدة وتحديد شفرة مصدر الماكرو.
auto module_ = System::MakeObject<Aspose::Words::Vba::VbaModule>();
module_->set_Name(u"Aspose.Module");
module_->set_Type(Aspose::Words::Vba::VbaModuleType::ProceduralModule);
module_->set_SourceCode(u"New source code");

// إضافة الوحدة إلى مشروع VBA.
doc->get_VbaProject()->get_Modules()->Add(module_);

doc->Save(get_ArtifactsDir() + u"VbaProject.CreateVBAMacros.docm");
```

## انظر أيضًا

* Class [VbaProject](../)
* Namespace [Aspose::Words::Vba](../../)
* Library [Aspose.Words for C++](../../../)
