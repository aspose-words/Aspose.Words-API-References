---
title: "طريقة Aspose::Words::Vba::VbaModuleCollection::get_Count"
linktitle: "get_Count"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Vba::VbaModuleCollection::get_Count. تُرجع عدد وحدات VBA في المجموعة في C++."
type: docs
weight: 7000
url: /ar/cpp/aspose.words.vba/vbamodulecollection/get_count/
---
## VbaModuleCollection::get_Count method


يعيد عدد وحدات VBA في المجموعة.

```cpp
int32_t Aspose::Words::Vba::VbaModuleCollection::get_Count()
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

## انظر أيضًا

* Class [VbaModuleCollection](../)
* Namespace [Aspose::Words::Vba](../../)
* Library [Aspose.Words for C++](../../../)
