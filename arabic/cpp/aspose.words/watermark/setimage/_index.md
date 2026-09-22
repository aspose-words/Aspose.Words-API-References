---
title: "Aspose::Words::Watermark::SetImage method"
linktitle: "SetImage"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Watermark::SetImage method. يضيف علامة مائية صورة إلى المستند في C++."
type: docs
weight: 6000
url: /ar/cpp/aspose.words/watermark/setimage/
---
## Watermark::SetImage(const System::SharedPtr\<System::Drawing::Image\>\&) method


يضيف علامة مائية صورة إلى المستند.

```cpp
void Aspose::Words::Watermark::SetImage(const System::SharedPtr<System::Drawing::Image> &image)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| image | const System::SharedPtr\<System::Drawing::Image\>\& | الصورة المعروضة كعلامة مائية. |

## أمثلة



يوضح كيفية إنشاء علامة مائية من صورة في نظام الملفات المحلي.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// عدّل مظهر العلامة المائية للصورة باستخدام كائن ImageWatermarkOptions،
// ثم مرره أثناء إنشاء علامة مائية من ملف صورة.
auto imageWatermarkOptions = System::MakeObject<Aspose::Words::ImageWatermarkOptions>();
imageWatermarkOptions->set_Scale(5);
imageWatermarkOptions->set_IsWashout(false);

// لدينا خيارات مختلفة لإدراج صورة.
// استخدم إحدى الطرق التالية لإضافة علامة مائية صورة.
doc->get_Watermark()->SetImage(System::Drawing::Image::FromFile(get_ImageDir() + u"Logo.jpg"));

doc->get_Watermark()->SetImage(System::Drawing::Image::FromFile(get_ImageDir() + u"Logo.jpg"), imageWatermarkOptions);

doc->get_Watermark()->SetImage(get_ImageDir() + u"Logo.jpg", imageWatermarkOptions);

doc->Save(get_ArtifactsDir() + u"Document.ImageWatermark.docx");
```

## انظر أيضًا

* Class [Watermark](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Watermark::SetImage(const System::SharedPtr\<System::Drawing::Image\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


يضيف علامة مائية صورة إلى المستند.

```cpp
void Aspose::Words::Watermark::SetImage(const System::SharedPtr<System::Drawing::Image> &image, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| image | const System::SharedPtr\<System::Drawing::Image\>\& | الصورة المعروضة كعلامة مائية. |
| خيارات | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | يحدد خيارات إضافية للعلامة المائية الصورة. |

## أمثلة



يوضح كيفية إنشاء علامة مائية من صورة في نظام الملفات المحلي.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// عدّل مظهر العلامة المائية للصورة باستخدام كائن ImageWatermarkOptions،
// ثم مرره أثناء إنشاء علامة مائية من ملف صورة.
auto imageWatermarkOptions = System::MakeObject<Aspose::Words::ImageWatermarkOptions>();
imageWatermarkOptions->set_Scale(5);
imageWatermarkOptions->set_IsWashout(false);

// لدينا خيارات مختلفة لإدراج صورة.
// استخدم إحدى الطرق التالية لإضافة علامة مائية صورة.
doc->get_Watermark()->SetImage(System::Drawing::Image::FromFile(get_ImageDir() + u"Logo.jpg"));

doc->get_Watermark()->SetImage(System::Drawing::Image::FromFile(get_ImageDir() + u"Logo.jpg"), imageWatermarkOptions);

doc->get_Watermark()->SetImage(get_ImageDir() + u"Logo.jpg", imageWatermarkOptions);

doc->Save(get_ArtifactsDir() + u"Document.ImageWatermark.docx");
```

## انظر أيضًا

* Class [ImageWatermarkOptions](../../imagewatermarkoptions/)
* Class [Watermark](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Watermark::SetImage(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


يضيف علامة مائية صورة إلى المستند.

```cpp
void Aspose::Words::Watermark::SetImage(const System::SharedPtr<System::IO::Stream> &imageStream, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| imageStream | const System::SharedPtr\<System::IO::Stream\>\& | الدفق الذي يحتوي على بيانات الصورة المعروضة كعلامة مائية. |
| خيارات | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | يحدد خيارات إضافية للعلامة المائية الصورة. |

## أمثلة



يظهر كيفية إنشاء علامة مائية من دفق صورة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// عدّل مظهر العلامة المائية للصورة باستخدام كائن ImageWatermarkOptions،
// ثم مرره أثناء إنشاء علامة مائية من ملف صورة.
auto imageWatermarkOptions = System::MakeObject<Aspose::Words::ImageWatermarkOptions>();
imageWatermarkOptions->set_Scale(5);

{
    auto imageStream = System::MakeObject<System::IO::FileStream>(get_ImageDir() + u"Logo.jpg", System::IO::FileMode::Open, System::IO::FileAccess::Read);
    doc->get_Watermark()->SetImage(imageStream, imageWatermarkOptions);
}

doc->Save(get_ArtifactsDir() + u"Document.ImageWatermarkStream.docx");
```

## انظر أيضًا

* Class [ImageWatermarkOptions](../../imagewatermarkoptions/)
* Class [Watermark](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Watermark::SetImage(const System::String\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


يضيف علامة مائية صورة إلى المستند.

```cpp
void Aspose::Words::Watermark::SetImage(const System::String &imagePath, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| imagePath | const System::String\& | المسار إلى ملف الصورة المعروض كعلامة مائية. |
| خيارات | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | يحدد خيارات إضافية للعلامة المائية الصورة. |

## أمثلة



يوضح كيفية إنشاء علامة مائية من صورة في نظام الملفات المحلي.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// عدّل مظهر العلامة المائية للصورة باستخدام كائن ImageWatermarkOptions،
// ثم مرره أثناء إنشاء علامة مائية من ملف صورة.
auto imageWatermarkOptions = System::MakeObject<Aspose::Words::ImageWatermarkOptions>();
imageWatermarkOptions->set_Scale(5);
imageWatermarkOptions->set_IsWashout(false);

// لدينا خيارات مختلفة لإدراج صورة.
// استخدم إحدى الطرق التالية لإضافة علامة مائية صورة.
doc->get_Watermark()->SetImage(System::Drawing::Image::FromFile(get_ImageDir() + u"Logo.jpg"));

doc->get_Watermark()->SetImage(System::Drawing::Image::FromFile(get_ImageDir() + u"Logo.jpg"), imageWatermarkOptions);

doc->get_Watermark()->SetImage(get_ImageDir() + u"Logo.jpg", imageWatermarkOptions);

doc->Save(get_ArtifactsDir() + u"Document.ImageWatermark.docx");
```

## انظر أيضًا

* Class [ImageWatermarkOptions](../../imagewatermarkoptions/)
* Class [Watermark](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
