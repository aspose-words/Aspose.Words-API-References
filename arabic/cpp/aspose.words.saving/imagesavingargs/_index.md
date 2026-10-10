---
title: "فئة Aspose::Words::Saving::ImageSavingArgs"
linktitle: "ImageSavingArgs"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::Saving::ImageSavingArgs. توفر بيانات لحدث ImageSaving(). لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 12000
url: /ar/cpp/aspose.words.saving/imagesavingargs/
---
## ImageSavingArgs class


توفر بيانات لحدث [ImageSaving()](../iimagesavingcallback/imagesaving/). لمعرفة المزيد، زر مقالة الوثائق [Save a Document](https://docs.aspose.com/words/cpp/save-a-document/).

```cpp
class ImageSavingArgs : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_CurrentShape](./get_currentshape/)() const | يحصل على كائن [ShapeBase](../../aspose.words.drawing/shapebase/) المقابل للشكل أو مجموعة الأشكال التي ستُحفظ قريبًا. |
| [get_Document](./get_document/)() | يحصل على كائن المستند الذي يتم حفظه حاليًا. |
| [get_ImageFileName](./get_imagefilename/)() const | يحصل أو يعيّن اسم الملف (بدون المسار) حيث سيتم حفظ الصورة. |
| [get_ImageStream](./get_imagestream/)() const | يسمح بتحديد الدفق الذي سيتم حفظ الصورة فيه. |
| [get_IsImageAvailable](./get_isimageavailable/)() const | يرجع **true** إذا كانت الصورة الحالية متاحة للتصدير. |
| [get_KeepImageStreamOpen](./get_keepimagestreamopen/)() const | يحدد ما إذا كان يجب على Aspose.Words إبقاء الدفق مفتوحًا أو إغلاقه بعد حفظ الصورة. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_ImageFileName](./set_imagefilename/)(const System::String\&) | مُعيّن لـ [Aspose::Words::Saving::ImageSavingArgs::get_ImageFileName](./get_imagefilename/). |
| [set_ImageStream](./set_imagestream/)(const System::SharedPtr\<System::IO::Stream\>\&) | المحدد لـ [Aspose::Words::Saving::ImageSavingArgs::get_ImageStream](./get_imagestream/). |
| [set_ImageStream](./set_imagestream/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| [set_KeepImageStreamOpen](./set_keepimagestreamopen/)(bool) | المحدد لـ [Aspose::Words::Saving::ImageSavingArgs::get_KeepImageStreamOpen](./get_keepimagestreamopen/). |
| static [Type](./type/)() |  |
## ملاحظات


بشكل افتراضي، عندما تقوم Aspose.Words بحفظ مستند إلى HTML، فإنها تحفظ كل صورة في ملف منفصل. تستخدم Aspose.Words اسم ملف المستند ورقمًا فريدًا لإنشاء اسم ملف فريد لكل صورة موجودة في المستند.

[ImageSavingArgs](./) allows to redefine how image file names are generated or to completely circumvent saving of images into files by providing your own stream objects.

لتطبيق المنطق الخاص بك لتوليد أسماء ملفات الصور، استخدم الخصائص [ImageFileName](./get_imagefilename/)، [CurrentShape](./get_currentshape/) و [IsImageAvailable](./get_isimageavailable/).

لحفظ الصور في تدفقات بدلاً من ملفات، استخدم الخاصية [ImageStream](./get_imagestream/).
## انظر أيضًا

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
