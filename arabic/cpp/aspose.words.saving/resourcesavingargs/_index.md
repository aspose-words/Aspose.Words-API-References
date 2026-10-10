---
title: "Aspose::Words::Saving::ResourceSavingArgs class"
linktitle: "ResourceSavingArgs"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::Saving::ResourceSavingArgs. توفر بيانات لحدث ResourceSaving(). لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 27000
url: /ar/cpp/aspose.words.saving/resourcesavingargs/
---
## ResourceSavingArgs class


توفر بيانات لحدث [ResourceSaving()](../iresourcesavingcallback/resourcesaving/). لمعرفة المزيد، زر مقالة الوثائق [Save a Document](https://docs.aspose.com/words/cpp/save-a-document/).

```cpp
class ResourceSavingArgs : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_Document](./get_document/)() const | يحصل على كائن المستند الذي يتم حفظه حاليًا. |
| [get_KeepResourceStreamOpen](./get_keepresourcestreamopen/)() const | يحدد ما إذا كان Aspose.Words يجب أن يبقي الدفق مفتوحًا أو يغلقه بعد حفظ المورد. |
| [get_ResourceFileName](./get_resourcefilename/)() const | يحصل أو يعيّن اسم الملف (بدون المسار) حيث سيتم حفظ المورد. |
| [get_ResourceFileUri](./get_resourcefileuri/)() const | يحصل أو يعيّن معرف المورد الموحد (URI) المستخدم للإشارة إلى ملف المورد من المستند. |
| [get_ResourceStream](./get_resourcestream/)() const | يسمح بتحديد الدفق الذي سيتم حفظ المورد فيه. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_KeepResourceStreamOpen](./set_keepresourcestreamopen/)(bool) | مُعيّن لـ [Aspose::Words::Saving::ResourceSavingArgs::get_KeepResourceStreamOpen](./get_keepresourcestreamopen/). |
| [set_ResourceFileName](./set_resourcefilename/)(const System::String\&) | مُعيّن لـ [Aspose::Words::Saving::ResourceSavingArgs::get_ResourceFileName](./get_resourcefilename/). |
| [set_ResourceFileUri](./set_resourcefileuri/)(const System::String\&) | مُعيّن لـ [Aspose::Words::Saving::ResourceSavingArgs::get_ResourceFileUri](./get_resourcefileuri/). |
| [set_ResourceStream](./set_resourcestream/)(const System::SharedPtr\<System::IO::Stream\>\&) | مُعيّن لـ [Aspose::Words::Saving::ResourceSavingArgs::get_ResourceStream](./get_resourcestream/). |
| [set_ResourceStream](./set_resourcestream/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| static [Type](./type/)() |  |
## ملاحظات


بشكل افتراضي، عندما يقوم Aspose.Words بحفظ مستند إلى HTML ثابت الصفحة أو SVG أو Markdown، فإنه يحفظ كل مورد في ملف منفصل. يستخدم Aspose.Words اسم ملف المستند ورقمًا فريدًا لإنشاء اسم ملف فريد لكل مورد موجود في المستند.

[ResourceSavingArgs](./) allows to redefine how resource file names are generated or to completely circumvent saving of resources into files by providing your own stream objects.

لتطبيق منطقك الخاص لتوليد أسماء ملفات الموارد، استخدم الخاصية [ResourceFileName](./get_resourcefilename/).

لحفظ الموارد في تدفقات بدلاً من الملفات، استخدم الخاصية [ResourceStream](./get_resourcestream/).
## انظر أيضًا

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
