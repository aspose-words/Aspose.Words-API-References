---
title: "Aspose::Words::Vba::VbaProject class"
linktitle: "VbaProject"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::Vba::VbaProject. توفر الوصول إلى معلومات مشروع VBA. يُعرّف مشروع VBA داخل المستند على أنه مجموعة من وحدات VBA. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.vba/vbaproject/
---
## VbaProject class


يوفر الوصول إلى معلومات مشروع VBA. يُعرّف مشروع VBA داخل المستند كمجموعة من وحدات VBA. لمعرفة المزيد، زر مقالة الوثائق [العمل مع ماكرو VBA](https://docs.aspose.com/words/cpp/working-with-vba-macros/).

```cpp
class VbaProject : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [Clone](./clone/)() | يقوم بعمل نسخة من [VbaProject](./). |
| [get_CodePage](./get_codepage/)() const | يحصل أو يضبط صفحة الترميز لمشروع VBA. |
| [get_IsProtected](./get_isprotected/)() | يظهر ما إذا كان [VbaProject](./) محميًا بكلمة مرور. |
| [get_IsSigned](./get_issigned/)() | يظهر ما إذا كان [VbaProject](./) موقّعًا أم لا. |
| [get_Modules](./get_modules/)() | يرجع مجموعة من وحدات مشروع VBA. |
| [get_Name](./get_name/)() const | يحصل أو يضبط اسم مشروع VBA. |
| [get_References](./get_references/)() | يحصل على مجموعة من مراجع مشروع VBA. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_CodePage](./set_codepage/)(int32_t) | مُعيّن لـ [Aspose::Words::Vba::VbaProject::get_CodePage](./get_codepage/). |
| [set_Name](./set_name/)(const System::String\&) | مُعيّن لـ [Aspose::Words::Vba::VbaProject::get_Name](./get_name/). |
| static [Type](./type/)() |  |
| [VbaProject](./vbaproject/)() | ينشئ [VbaProject](./) فارغًا. |

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

* Namespace [Aspose::Words::Vba](../)
* Library [Aspose.Words for C++](../../)
