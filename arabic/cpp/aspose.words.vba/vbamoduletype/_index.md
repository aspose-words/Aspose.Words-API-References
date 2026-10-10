---
title: "Aspose::Words::Vba::VbaModuleType enum"
linktitle: "VbaModuleType"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Vba::VbaModuleType enum. يحدد نوع نموذج في مشروع VBA في C++."
type: docs
weight: 6000
url: /ar/cpp/aspose.words.vba/vbamoduletype/
---
## VbaModuleType enum


يحدد نوع النموذج في مشروع VBA.

```cpp
enum class VbaModuleType
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| DocumentModule | 0 | نوع من عناصر مشروع VBA يحدد وحدة للماكرو المدمجة وعمليات الوصول البرمجي المرتبطة بمستند. |
| ProceduralModule | 1 | مجموعة من الروتينات الفرعية والدوال. |
| ClassModule | 2 | وحدة تحتوي على تعريف كائن جديد. كل نسخة من الفئة تنشئ كائنًا جديدًا، وتصبح الإجراءات المعرفة في الوحدة خصائص وأساليب لهذا الكائن. |
| DesignerModule | 3 | وحدة VBA تُوسّع الأساليب والخصائص لعنصر تحكم ActiveX تم تسجيله في المشروع. |


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

* Namespace [Aspose::Words::Vba](../)
* Library [Aspose.Words for C++](../../)
