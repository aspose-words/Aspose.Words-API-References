---
title: "Aspose::Words::Saving::ImageSaveOptions::get_JpegQuality طريقة"
linktitle: "get_JpegQuality"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::ImageSaveOptions::get_JpegQuality طريقة. يحصل على أو يضبط قيمة تحدد جودة صور JPEG المُولدة في C++."
type: docs
weight: 8000
url: /ar/cpp/aspose.words.saving/imagesaveoptions/get_jpegquality/
---
## ImageSaveOptions::get_JpegQuality method


يحصل أو يضبط قيمة تحدد جودة صور JPEG المُولَّدة.

```cpp
int32_t Aspose::Words::Saving::ImageSaveOptions::get_JpegQuality()
```

## ملاحظات


يكون له تأثير فقط عند الحفظ إلى JPEG.

استخدم هذه الخاصية للحصول على أو ضبط جودة الصور المُولدة عند الحفظ بصيغة JPEG. قد تتراوح القيمة من 0 إلى 100 حيث يعني 0 أسوأ جودة لكن أقصى ضغط و100 يعني أفضل جودة لكن أقل ضغط.

القيمة الافتراضية هي 95.

## أمثلة



يوضح كيفية تكوين الضغط أثناء حفظ المستند كملف JPEG.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// إنشاء كائن "ImageSaveOptions" يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
// لتعديل الطريقة التي تقوم بها تلك الطريقة بتحويل المستند إلى صورة.
auto imageOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Jpeg);
// اضبط الخاصية "JpegQuality" إلى "10" لاستخدام ضغط أقوى عند تحويل المستند.
// سيؤدي ذلك إلى تقليل حجم ملف المستند، لكن الصورة ستظهر آثار ضغط أكثر وضوحًا.
imageOptions->set_JpegQuality(10);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.JpegQuality.HighCompression.jpg", imageOptions);

// اضبط الخاصية "JpegQuality" إلى "100" لاستخدام ضغط أضعف عند rending المستند.
// سيحسن ذلك جودة الصورة على حساب زيادة حجم الملف.
imageOptions->set_JpegQuality(100);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.JpegQuality.HighQuality.jpg", imageOptions);
```

## انظر أيضًا

* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
