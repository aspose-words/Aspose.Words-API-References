---
title: "فئة Aspose::Words::FileFormatUtil"
linktitle: "FileFormatUtil"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::FileFormatUtil. توفر طرقًا مساعدة للعمل مع صيغ الملفات، مثل اكتشاف صيغة الملف أو تحويل امتدادات الملفات إلى/من تعداد صيغ الملفات. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 28000
url: /ar/cpp/aspose.words/fileformatutil/
---
## FileFormatUtil class


يوفر طرقًا مساعدة للعمل مع صيغ الملفات، مثل اكتشاف صيغة الملف أو تحويل امتدادات الملفات إلى/من تعداد صيغ الملفات. لمعرفة المزيد، زر مقالة الوثائق [Detect File Format and Check Format Compatibility](https://docs.aspose.com/words/cpp/detect-file-format-and-check-format-compatibility/)

```cpp
class FileFormatUtil
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| static [ContentTypeToLoadFormat](./contenttypetoloadformat/)(const System::String\&) | يحوّل نوع محتوى IANA إلى قيمة تعداد صيغة التحميل. |
| static [ContentTypeToSaveFormat](./contenttypetosaveformat/)(const System::String\&) | يحوّل نوع محتوى IANA إلى قيمة تعداد صيغة الحفظ. |
| static [DetectFileFormat](./detectfileformat/)(const System::String\&) | يكشف ويعيد المعلومات حول صيغة مستند مخزن في ملف على القرص. |
| static [DetectFileFormat](./detectfileformat/)(const System::SharedPtr\<System::IO::Stream\>\&) | يكشف ويعيد المعلومات حول صيغة مستند مخزن في تدفق. |
| static [DetectFileFormat](./detectfileformat/)(std::basic_istream\<CharType, Traits\>\&) |  |
| static [ExtensionToSaveFormat](./extensiontosaveformat/)(const System::String\&) | يحوّل امتداد اسم ملف إلى قيمة [SaveFormat](../saveformat/). |
| [FileFormatUtil](./fileformatutil/)() |  |
| static [ImageTypeToExtension](./imagetypetoextension/)(Aspose::Words::Drawing::ImageType) | يحوّل قيمة تعداد نوع صورة Aspose.Words إلى امتداد ملف. الامتداد المُرجع هو سلسلة بحروف صغيرة مع نقطة في البداية. |
| static [LoadFormatToExtension](./loadformattoextension/)(Aspose::Words::LoadFormat) | يحوّل قيمة تعداد صيغة التحميل إلى امتداد ملف. الامتداد المُرجع هو سلسلة بحروف صغيرة مع نقطة في البداية. |
| static [LoadFormatToSaveFormat](./loadformattosaveformat/)(Aspose::Words::LoadFormat) | يحوّل قيمة [LoadFormat](../loadformat/) إلى قيمة [SaveFormat](../saveformat/) إذا أمكن. |
| static [SaveFormatToExtension](./saveformattoextension/)(Aspose::Words::SaveFormat) | يحوّل قيمة تعداد صيغة الحفظ إلى امتداد ملف. الامتداد المُرجع هو سلسلة بحروف صغيرة مع نقطة في البداية. |
| static [SaveFormatToLoadFormat](./saveformattoloadformat/)(Aspose::Words::SaveFormat) | يحوّل قيمة [SaveFormat](../saveformat/) إلى قيمة [LoadFormat](../loadformat/) إذا أمكن. |

## أمثلة



يوضح كيفية اكتشاف الترميز في ملف html.
```cpp
System::SharedPtr<Aspose::Words::FileFormatInfo> info = Aspose::Words::FileFormatUtil::DetectFileFormat(get_MyDir() + u"Document.html");

ASSERT_EQ(Aspose::Words::LoadFormat::Html, info->get_LoadFormat());

// يُستخدم خاصية Encoding فقط عندما نقوم بإنشاء كائن FileFormatInfo لمستند html.
ASSERT_EQ(u"Western European (Windows)", info->get_Encoding()->get_EncodingName());
ASSERT_EQ(1252, info->get_Encoding()->get_CodePage());
```

## انظر أيضًا

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
