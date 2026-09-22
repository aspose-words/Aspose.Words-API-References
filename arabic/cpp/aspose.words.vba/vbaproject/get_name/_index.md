---
title: "طريقة Aspose::Words::Vba::VbaProject::get_Name"
linktitle: "get_Name"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Vba::VbaProject::get_Name. يحصل على أو يضبط اسم مشروع VBA في C++."
type: docs
weight: 7000
url: /ar/cpp/aspose.words.vba/vbaproject/get_name/
---
## VbaProject::get_Name method


يحصل أو يضبط اسم مشروع VBA.

```cpp
System::String Aspose::Words::Vba::VbaProject::get_Name() const
```


## أمثلة



يُظهر كيفية الوصول إلى معلومات مشروع VBA الخاص بالمستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"VBA project.docm");

// يحتوي مشروع VBA على مجموعة من وحدات VBA.
System::SharedPtr<Aspose::Words::Vba::VbaProject> vbaProject = doc->get_VbaProject();
std::cout << (vbaProject->get_IsSigned() ? System::String::Format(u"Project name: {0} signed; Project code page: {1}; Modules count: {2}\n", vbaProject->get_Name(), vbaProject->get_CodePage(), vbaProject->get_Modules()->LINQ_Count()) : System::String::Format(u"Project name: {0} not signed; Project code page: {1}; Modules count: {2}\n", vbaProject->get_Name(), vbaProject->get_CodePage(), vbaProject->get_Modules()->LINQ_Count())) << std::endl;

System::SharedPtr<Aspose::Words::Vba::VbaModuleCollection> vbaModules = doc->get_VbaProject()->get_Modules();

ASSERT_EQ(vbaModules->LINQ_Count(), 3);

for (auto&& module_ : vbaModules)
{
    std::cout << System::String::Format(u"Module name: {0};\nModule code:\n{1}\n", module_->get_Name(), module_->get_SourceCode()) << std::endl;
}

// تعيين شفرة مصدر جديدة لوحدة VBA. يمكنك الوصول إلى وحدات VBA في المجموعة إما عن طريق الفهرس أو بالاسم.
vbaModules->idx_get(0)->set_SourceCode(u"Your VBA code...");
vbaModules->idx_get(u"Module1")->set_SourceCode(u"Your VBA code...");

// إزالة وحدة من المجموعة.
vbaModules->Remove(vbaModules->idx_get(2));
```


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
