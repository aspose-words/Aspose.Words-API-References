---
title: "Aspose::Words::DocumentBuilder::InsertOnlineVideo طريقة"
linktitle: "InsertOnlineVideo"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::DocumentBuilder::InsertOnlineVideo طريقة. يُدرج كائن فيديو عبر الإنترنت في المستند ويُقِيسه إلى الحجم المحدد في C++."
type: docs
weight: 43000
url: /ar/cpp/aspose.words/documentbuilder/insertonlinevideo/
---
## DocumentBuilder::InsertOnlineVideo(const System::String\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method


يقوم بإدراج كائن فيديو عبر الإنترنت في المستند ويقوم بتحجيمه إلى الحجم المحدد.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOnlineVideo(const System::String &videoUrl, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| videoUrl | const System::String\& | عنوان URL للفيديو. |
| horzPos | Aspose::Words::Drawing::RelativeHorizontalPosition | يحدد من أين يُقاس المسافة إلى الصورة. |
| left | double | المسافة بالنقاط من الأصل إلى الجانب الأيسر من الصورة. |
| vertPos | Aspose::Words::Drawing::RelativeVerticalPosition | يحدد من أين تُقاس المسافة إلى الصورة. |
| top | double | المسافة بالنقاط من الأصل إلى الجانب العلوي من الصورة. |
| العرض | double | عرض الصورة بالنقاط. يمكن أن يكون قيمة سالبة أو صفر لطلب مقياس 100٪. |
| الارتفاع | double | ارتفاع الصورة بالنقاط. يمكن أن يكون قيمة سالبة أو صفر لطلب مقياس 100٪. |
| wrapType | Aspose::Words::Drawing::WrapType | يحدد كيفية لف النص حول الصورة. |

### ReturnValue

عقدة الصورة التي تم إدراجها للتو.
## ملاحظات


يمكنك تغيير حجم الصورة، موقعها، طريقة تموضعها وإعدادات أخرى باستخدام كائن [Shape](../../../aspose.words.drawing/shape/) الذي تُعيده هذه الطريقة.

يتم دعم إدراج فيديو عبر الإنترنت من الموارد التالية:

* [https://www.youtube.com/](https://www.youtube.com/)
* [https://vimeo.com/](https://vimeo.com/)



إذا لم يُعرض الفيديو عبر الإنترنت بشكل صحيح، استخدم [InsertOnlineVideo()](../)، الذي يقبل كود HTML مضمّن مخصص.

قد يختلف كود تضمين الفيديو بين المزودين، استشر المزود المناسب لك للحصول على التفاصيل.

## انظر أيضًا

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOnlineVideo(const System::String\&, const System::String\&, const System::ArrayPtr\<uint8_t\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method


يقوم بإدراج كائن فيديو عبر الإنترنت في المستند ويقوم بتحجيمه إلى الحجم المحدد.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOnlineVideo(const System::String &videoUrl, const System::String &videoEmbedCode, const System::ArrayPtr<uint8_t> &thumbnailImageBytes, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| videoUrl | const System::String\& | عنوان URL للفيديو. |
| videoEmbedCode | const System::String\& | كود التضمين للفيديو. |
| thumbnailImageBytes | const System::ArrayPtr\<uint8_t\>\& | بايتات صورة المصغّر. |
| horzPos | Aspose::Words::Drawing::RelativeHorizontalPosition | يحدد من أين يُقاس المسافة إلى الصورة. |
| left | double | المسافة بالنقاط من الأصل إلى الجانب الأيسر من الصورة. |
| vertPos | Aspose::Words::Drawing::RelativeVerticalPosition | يحدد من أين تُقاس المسافة إلى الصورة. |
| top | double | المسافة بالنقاط من الأصل إلى الجانب العلوي من الصورة. |
| العرض | double | عرض الصورة بالنقاط. يمكن أن يكون قيمة سالبة أو صفر لطلب مقياس 100٪. |
| الارتفاع | double | ارتفاع الصورة بالنقاط. يمكن أن يكون قيمة سالبة أو صفر لطلب مقياس 100٪. |
| wrapType | Aspose::Words::Drawing::WrapType | يحدد كيفية لف النص حول الصورة. |

### ReturnValue

عقدة الصورة التي تم إدراجها للتو.
## ملاحظات


يمكنك تغيير حجم الصورة، موقعها، طريقة تموضعها وإعدادات أخرى باستخدام كائن [Shape](../../../aspose.words.drawing/shape/) الذي تُعيده هذه الطريقة.

## أمثلة



يظهر كيفية إدراج فيديو عبر الإنترنت في مستند مع صورة مصغرة مخصصة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::String videoUrl = u"https://vimeo.com/52477838";
System::String videoEmbedCode = System::String(u"<iframe src=\"https://player.vimeo.com/video/52477838\" width=\"640\" height=\"360\" frameborder=\"0\" ") + u"title=\"Aspose\" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>";

System::ArrayPtr<uint8_t> thumbnailImageBytes = System::IO::File::ReadAllBytes(get_ImageDir() + u"Logo.jpg");

{
    auto stream = System::MakeObject<System::IO::MemoryStream>(thumbnailImageBytes);
    {
        System::SharedPtr<System::Drawing::Image> image = System::Drawing::Image::FromStream(stream);
        // فيما يلي طريقتان لإنشاء شكل بصورة مصغرة مخصصة، والتي ترتبط بفيديو على الإنترنت
        // سيتم تشغيله عندما نضغط على الشكل في Microsoft Word.
        // 1 -  إدراج شكل مضمن عند مؤشر إدخال عقدة الباني:
        builder->InsertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes, image->get_Width(), image->get_Height());

        builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

        // 2 -  إدراج شكل عائم:
        double left = builder->get_PageSetup()->get_RightMargin() - image->get_Width();
        double top = builder->get_PageSetup()->get_BottomMargin() - image->get_Height();

        builder->InsertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes, Aspose::Words::Drawing::RelativeHorizontalPosition::RightMargin, left, Aspose::Words::Drawing::RelativeVerticalPosition::BottomMargin, top, image->get_Width(), image->get_Height(), Aspose::Words::Drawing::WrapType::Square);
    }
}

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertOnlineVideoCustomThumbnail.docx");
```

## انظر أيضًا

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOnlineVideo(const System::String\&, const System::String\&, const System::ArrayPtr\<uint8_t\>\&, double, double) method


يقوم بإدراج كائن فيديو عبر الإنترنت في المستند ويقوم بتحجيمه إلى الحجم المحدد.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOnlineVideo(const System::String &videoUrl, const System::String &videoEmbedCode, const System::ArrayPtr<uint8_t> &thumbnailImageBytes, double width, double height)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| videoUrl | const System::String\& | عنوان URL للفيديو. |
| videoEmbedCode | const System::String\& | كود التضمين للفيديو. |
| thumbnailImageBytes | const System::ArrayPtr\<uint8_t\>\& | بايتات صورة المصغّر. |
| العرض | double | عرض الصورة بالنقاط. يمكن أن يكون قيمة سالبة أو صفر لطلب مقياس 100٪. |
| الارتفاع | double | ارتفاع الصورة بالنقاط. يمكن أن يكون قيمة سالبة أو صفر لطلب مقياس 100٪. |

### ReturnValue

عقدة الصورة التي تم إدراجها للتو.
## ملاحظات


يمكنك تغيير حجم الصورة، موقعها، طريقة تموضعها وإعدادات أخرى باستخدام كائن [Shape](../../../aspose.words.drawing/shape/) الذي تُعيده هذه الطريقة.

## أمثلة



يظهر كيفية إدراج فيديو عبر الإنترنت في مستند مع صورة مصغرة مخصصة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::String videoUrl = u"https://vimeo.com/52477838";
System::String videoEmbedCode = System::String(u"<iframe src=\"https://player.vimeo.com/video/52477838\" width=\"640\" height=\"360\" frameborder=\"0\" ") + u"title=\"Aspose\" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>";

System::ArrayPtr<uint8_t> thumbnailImageBytes = System::IO::File::ReadAllBytes(get_ImageDir() + u"Logo.jpg");

{
    auto stream = System::MakeObject<System::IO::MemoryStream>(thumbnailImageBytes);
    {
        System::SharedPtr<System::Drawing::Image> image = System::Drawing::Image::FromStream(stream);
        // فيما يلي طريقتان لإنشاء شكل بصورة مصغرة مخصصة، والتي ترتبط بفيديو على الإنترنت
        // سيتم تشغيله عندما نضغط على الشكل في Microsoft Word.
        // 1 -  إدراج شكل مضمن عند مؤشر إدخال عقدة الباني:
        builder->InsertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes, image->get_Width(), image->get_Height());

        builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

        // 2 -  إدراج شكل عائم:
        double left = builder->get_PageSetup()->get_RightMargin() - image->get_Width();
        double top = builder->get_PageSetup()->get_BottomMargin() - image->get_Height();

        builder->InsertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes, Aspose::Words::Drawing::RelativeHorizontalPosition::RightMargin, left, Aspose::Words::Drawing::RelativeVerticalPosition::BottomMargin, top, image->get_Width(), image->get_Height(), Aspose::Words::Drawing::WrapType::Square);
    }
}

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertOnlineVideoCustomThumbnail.docx");
```

## انظر أيضًا

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOnlineVideo(const System::String\&, double, double) method


يقوم بإدراج كائن فيديو عبر الإنترنت في المستند ويقوم بتحجيمه إلى الحجم المحدد.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOnlineVideo(const System::String &videoUrl, double width, double height)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| videoUrl | const System::String\& | عنوان URL للفيديو. |
| العرض | double | عرض الصورة بالنقاط. يمكن أن يكون قيمة سالبة أو صفر لطلب مقياس 100٪. |
| الارتفاع | double | ارتفاع الصورة بالنقاط. يمكن أن يكون قيمة سالبة أو صفر لطلب مقياس 100٪. |

### ReturnValue

عقدة الصورة التي تم إدراجها للتو.
## ملاحظات


يمكنك تغيير حجم الصورة، موقعها، طريقة تموضعها وإعدادات أخرى باستخدام كائن [Shape](../../../aspose.words.drawing/shape/) الذي تُعيده هذه الطريقة.

يتم دعم إدراج فيديو عبر الإنترنت من الموارد التالية:

* [https://www.youtube.com/](https://www.youtube.com/)
* [https://vimeo.com/](https://vimeo.com/)



إذا لم يُعرض الفيديو عبر الإنترنت بشكل صحيح، استخدم [InsertOnlineVideo()](../)، الذي يقبل كود HTML مضمّن مخصص.

قد يختلف كود تضمين الفيديو بين المزودين، استشر المزود المناسب لك للحصول على التفاصيل.

## أمثلة



يظهر كيفية إدراج فيديو على الإنترنت في مستند باستخدام عنوان URL.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertOnlineVideo(u"https://youtu.be/g1N9ke8Prmk", 360, 270);

// يمكننا مشاهدة الفيديو من Microsoft Word بالنقر على الشكل.
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertVideoWithUrl.docx");
```

## انظر أيضًا

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
