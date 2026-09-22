---
title: "Aspose::Words::Saving::ImageSaveOptions::ImageSaveOptions مُنشئ"
linktitle: "ImageSaveOptions"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::ImageSaveOptions::ImageSaveOptions مُنشئ. يهيئ مثيلًا جديدًا من هذه الفئة يمكن استخدامه لحفظ الصور المرسومة بتنسيق Tiff أو Png أو Bmp أو Jpeg أو Emf أو Eps أو WebP أو Svg في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.saving/imagesaveoptions/imagesaveoptions/
---
## ImageSaveOptions::ImageSaveOptions constructor


يُهيئ مثيلًا جديدًا من هذه الفئة يمكن استخدامه لحفظ الصور المرسومة بتنسيق [Tiff](../../../aspose.words/saveformat/), [Png](../../../aspose.words/saveformat/), [Bmp](../../../aspose.words/saveformat/), [Jpeg](../../../aspose.words/saveformat/), [Emf](../../../aspose.words/saveformat/), [Eps](../../../aspose.words/saveformat/), [WebP](../) أو [Svg](../../../aspose.words/saveformat/) format.

```cpp
Aspose::Words::Saving::ImageSaveOptions::ImageSaveOptions(Aspose::Words::SaveFormat saveFormat)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| saveFormat | Aspose::Words::SaveFormat | يمكن أن يكون بتنسيق [Tiff](../../../aspose.words/saveformat/), [Png](../../../aspose.words/saveformat/), [Bmp](../../../aspose.words/saveformat/), [Jpeg](../../../aspose.words/saveformat/), [Emf](../../../aspose.words/saveformat/), [Eps](../../../aspose.words/saveformat/)[WebP](../) أو [Svg](../../../aspose.words/saveformat/) format. |

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

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
