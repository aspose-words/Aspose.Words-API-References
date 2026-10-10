---
title: "طريقة Aspose::Words::Vba::VbaModule::get_Type"
linktitle: "get_Type"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Vba::VbaModule::get_Type. تحدد ما إذا كانت الوحدة وحدة إجرائية، أو وحدة مستند، أو وحدة فئة، أو وحدة مصمم في C++."
type: docs
weight: 6000
url: /ar/cpp/aspose.words.vba/vbamodule/get_type/
---
## VbaModule::get_Type method


يحدد ما إذا كانت الوحدة وحدة إجرائية، أو وحدة مستند، أو وحدة فئة، أو وحدة مصمم.

```cpp
Aspose::Words::Vba::VbaModuleType Aspose::Words::Vba::VbaModule::get_Type() const
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

* Enum [VbaModuleType](../../vbamoduletype/)
* Class [VbaModule](../)
* Namespace [Aspose::Words::Vba](../../)
* Library [Aspose.Words for C++](../../../)
