---
title: "Aspose::Words::Saving::FontSavingArgs class"
linktitle: "FontSavingArgs"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::FontSavingArgs class. يوفر بيانات لحدث FontSaving(). لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 8000
url: /ar/cpp/aspose.words.saving/fontsavingargs/
---
## FontSavingArgs class


يوفر بيانات لحدث [FontSaving()](../ifontsavingcallback/fontsaving/). لمعرفة المزيد، زر مقالة الوثائق [Save a Document](https://docs.aspose.com/words/cpp/save-a-document/).

```cpp
class FontSavingArgs : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_Bold](./get_bold/)() const | يشير إلى ما إذا كان الخط الحالي غامقًا. |
| [get_Document](./get_document/)() const | يحصل على كائن المستند الذي يتم حفظه. |
| [get_FontFamilyName](./get_fontfamilyname/)() const | يشير إلى اسم عائلة الخط الحالي. |
| [get_FontFileName](./get_fontfilename/)() const | يحصل أو يعيّن اسم الملف (بدون المسار) حيث سيتم حفظ الخط. |
| [get_FontStream](./get_fontstream/)() const | يسمح بتحديد الدفق الذي سيتم حفظ الخط إليه. |
| [get_IsExportNeeded](./get_isexportneeded/)() const | يسمح بتحديد ما إذا كان الخط الحالي سيُصدّر كموارد خط. القيمة الافتراضية هي **true**. |
| [get_IsSubsettingNeeded](./get_issubsettingneeded/)() const | يسمح بتحديد ما إذا كان الخط الحالي سيُقسم إلى مجموعة فرعية قبل تصديره كموارد خط. |
| [get_Italic](./get_italic/)() const | يشير إلى ما إذا كان الخط الحالي مائلًا. |
| [get_KeepFontStreamOpen](./get_keepfontstreamopen/)() const | يحدد ما إذا كان Aspose.Words يجب أن يبقي الدفق مفتوحًا أم يغلقه بعد حفظ الخط. |
| [get_OriginalFileName](./get_originalfilename/)() const | يحصل على اسم ملف الخط الأصلي مع الامتداد. |
| [get_OriginalFileSize](./get_originalfilesize/)() const | يحصل على حجم ملف الخط الأصلي. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_FontFileName](./set_fontfilename/)(const System::String\&) | مُعيّن لـ [Aspose::Words::Saving::FontSavingArgs::get_FontFileName](./get_fontfilename/). |
| [set_FontStream](./set_fontstream/)(const System::SharedPtr\<System::IO::Stream\>\&) | مُعيّن لـ [Aspose::Words::Saving::FontSavingArgs::get_FontStream](./get_fontstream/). |
| [set_FontStream](./set_fontstream/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| [set_IsExportNeeded](./set_isexportneeded/)(bool) | يسمح بتحديد ما إذا كان الخط الحالي سيُصدّر كموارد خط. القيمة الافتراضية هي **true**. |
| [set_IsSubsettingNeeded](./set_issubsettingneeded/)(bool) | مُعيّن لـ [Aspose::Words::Saving::FontSavingArgs::get_IsSubsettingNeeded](./get_issubsettingneeded/). |
| [set_KeepFontStreamOpen](./set_keepfontstreamopen/)(bool) | مُعيّن لـ [Aspose::Words::Saving::FontSavingArgs::get_KeepFontStreamOpen](./get_keepfontstreamopen/). |
| static [Type](./type/)() |  |
## ملاحظات


عند قيام Aspose.Words بحفظ مستند إلى HTML أو صيغ ذات صلة و[ExportFontResources](../htmlsaveoptions/get_exportfontresources/) مُعيّن إلى **true**، فإنه يحفظ كل خط مخصص للتصدير في ملف منفصل.

[FontSavingArgs](./) controls whether particular font resource should be exported and how.

[FontSavingArgs](./) also allows to redefine how font file names are generated or to completely circumvent saving of fonts into files by providing your own stream objects.

لتحديد ما إذا كان يجب حفظ مورد خط معين، استخدم الخاصية [IsExportNeeded](./get_isexportneeded/).

لحفظ الخطوط في تدفقات بدلاً من ملفات، استخدم الخاصية [FontStream](./get_fontstream/).
## انظر أيضًا

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
