---
title: "Aspose::Words::Vba::VbaModule class"
linktitle: "VbaModule"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Vba::VbaModule class. يوفّر الوصول إلى وحدة مشروع VBA. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 1000
url: /ar/cpp/aspose.words.vba/vbamodule/
---
## VbaModule class


يوفر الوصول إلى وحدة مشروع VBA. لمعرفة المزيد، زر مقالة الوثائق [العمل مع ماكرو VBA](https://docs.aspose.com/words/cpp/working-with-vba-macros/).

```cpp
class VbaModule : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [Clone](./clone/)() | ينفّذ نسخة من [VbaModule](./). |
| [get_Name](./get_name/)() const | يحصل أو يعيّن اسم وحدة مشروع VBA. |
| [get_SourceCode](./get_sourcecode/)() const | يحصل أو يعيّن شفرة مصدر وحدة مشروع VBA. |
| [get_Type](./get_type/)() const | يحدد ما إذا كانت الوحدة وحدة إجرائية، أو وحدة مستند، أو وحدة فئة، أو وحدة مصمم. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Name](./set_name/)(const System::String\&) | مُعيّن لـ [Aspose::Words::Vba::VbaModule::get_Name](./get_name/). |
| [set_SourceCode](./set_sourcecode/)(const System::String\&) | مُعيّن لـ [Aspose::Words::Vba::VbaModule::get_SourceCode](./get_sourcecode/). |
| [set_Type](./set_type/)(Aspose::Words::Vba::VbaModuleType) | مُعيّن لـ [Aspose::Words::Vba::VbaModule::get_Type](./get_type/). |
| static [Type](./type/)() |  |
| [VbaModule](./vbamodule/)() | ينشئ وحدة فارغة. |

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
