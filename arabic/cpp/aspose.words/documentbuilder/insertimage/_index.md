---
title: "Aspose::Words::DocumentBuilder::InsertImage method"
linktitle: "InsertImage"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::DocumentBuilder::InsertImage. تُدرج صورة من مصفوفة بايتات إلى المستند. تُدرج الصورة داخل السطر وبنسبة 100% في C++."
type: docs
weight: 39000
url: /ar/cpp/aspose.words/documentbuilder/insertimage/
---
## DocumentBuilder::InsertImage(const System::ArrayPtr\<uint8_t\>\&) method


يقوم بإدراج صورة من مصفوفة بايتات في المستند. يتم إدراج الصورة داخل السطر وبنسبة 100٪.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::ArrayPtr<uint8_t> &imageBytes)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| imageBytes | const System::ArrayPtr\<uint8_t\>\& | مصفوفة البايتات التي تحتوي على الصورة. |

### ReturnValue

عقدة الصورة التي تم إدراجها للتو.
## ملاحظات


يمكنك تغيير حجم الصورة، موقعها، طريقة تموضعها وإعدادات أخرى باستخدام كائن [Shape](../../../aspose.words.drawing/shape/) الذي تُعيده هذه الطريقة.

## أمثلة



يظهر كيفية إدراج صورة من مصفوفة بايتات إلى مستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::ArrayPtr<uint8_t> imageByteArray = Aspose::Words::ApiExamples::TestUtil::ImageToByteArray(get_ImageDir() + u"Logo.jpg");

// فيما يلي ثلاث طرق لإدراج صورة من مصفوفة بايتات.
// 1 -  شكل مضمن بحجم افتراضي يعتمد على أبعاد الصورة الأصلية:
builder->InsertImage(imageByteArray);

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 2 -  شكل مضمن بأبعاد مخصصة:
builder->InsertImage(imageByteArray, Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 3 -  شكل عائم بأبعاد مخصصة:
builder->InsertImage(imageByteArray, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromByteArray.docx");
```

## انظر أيضًا

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::ArrayPtr\<uint8_t\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method


يقوم بإدراج صورة من مصفوفة بايتات في الموضع والحجم المحددين.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::ArrayPtr<uint8_t> &imageBytes, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| imageBytes | const System::ArrayPtr\<uint8_t\>\& | مصفوفة البايتات التي تحتوي على الصورة. |
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



يظهر كيفية إدراج صورة من مصفوفة بايتات إلى مستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::ArrayPtr<uint8_t> imageByteArray = Aspose::Words::ApiExamples::TestUtil::ImageToByteArray(get_ImageDir() + u"Logo.jpg");

// فيما يلي ثلاث طرق لإدراج صورة من مصفوفة بايتات.
// 1 -  شكل مضمن بحجم افتراضي يعتمد على أبعاد الصورة الأصلية:
builder->InsertImage(imageByteArray);

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 2 -  شكل مضمن بأبعاد مخصصة:
builder->InsertImage(imageByteArray, Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 3 -  شكل عائم بأبعاد مخصصة:
builder->InsertImage(imageByteArray, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromByteArray.docx");
```

## انظر أيضًا

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::ArrayPtr\<uint8_t\>\&, double, double) method


يقوم بإدراج صورة داخلية من مصفوفة بايتات في المستند ويقوم بتحجيمها إلى الحجم المحدد.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::ArrayPtr<uint8_t> &imageBytes, double width, double height)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| imageBytes | const System::ArrayPtr\<uint8_t\>\& | مصفوفة البايتات التي تحتوي على الصورة. |
| العرض | double | عرض الصورة بالنقاط. يمكن أن يكون قيمة سالبة أو صفر لطلب مقياس 100٪. |
| الارتفاع | double | ارتفاع الصورة بالنقاط. يمكن أن يكون قيمة سالبة أو صفر لطلب مقياس 100٪. |

### ReturnValue

عقدة الصورة التي تم إدراجها للتو.
## ملاحظات


يمكنك تغيير حجم الصورة، موقعها، طريقة تموضعها وإعدادات أخرى باستخدام كائن [Shape](../../../aspose.words.drawing/shape/) الذي تُعيده هذه الطريقة.

## أمثلة



يظهر كيفية إدراج صورة من مصفوفة بايتات إلى مستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::ArrayPtr<uint8_t> imageByteArray = Aspose::Words::ApiExamples::TestUtil::ImageToByteArray(get_ImageDir() + u"Logo.jpg");

// فيما يلي ثلاث طرق لإدراج صورة من مصفوفة بايتات.
// 1 -  شكل مضمن بحجم افتراضي يعتمد على أبعاد الصورة الأصلية:
builder->InsertImage(imageByteArray);

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 2 -  شكل مضمن بأبعاد مخصصة:
builder->InsertImage(imageByteArray, Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 3 -  شكل عائم بأبعاد مخصصة:
builder->InsertImage(imageByteArray, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromByteArray.docx");
```

## انظر أيضًا

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::SharedPtr\<System::Drawing::Image\>\&) method


يقوم بإدراج صورة من كائن **Image** في المستند. يتم إدراج الصورة داخل السطر وبنسبة 100٪.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::SharedPtr<System::Drawing::Image> &image)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| image | const System::SharedPtr\<System::Drawing::Image\>\& | الصورة التي سيتم إدراجها في المستند. |

### ReturnValue

عقدة الصورة التي تم إدراجها للتو.
## ملاحظات


يمكنك تغيير حجم الصورة، موقعها، طريقة تموضعها وإعدادات أخرى باستخدام كائن [Shape](../../../aspose.words.drawing/shape/) الذي تُعيده هذه الطريقة.

## أمثلة



يظهر كيفية إدراج صورة من كائن إلى مستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::String imageFile = get_ImageDir() + u"Logo.jpg";

// فيما يلي ثلاث طرق لإدراج صورة من نسخة كائن Image.
// 1 -  شكل مضمن بحجم افتراضي يعتمد على أبعاد الصورة الأصلية:
builder->InsertImage(imageFile);

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 2 -  شكل مضمن بأبعاد مخصصة:
builder->InsertImage(imageFile, Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 3 -  شكل عائم بأبعاد مخصصة:
builder->InsertImage(imageFile, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromImageObject.docx");
```

## انظر أيضًا

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::SharedPtr\<System::Drawing::Image\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method


يقوم بإدراج صورة من كائن **Image** في الموضع والحجم المحددين.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::SharedPtr<System::Drawing::Image> &image, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| image | const System::SharedPtr\<System::Drawing::Image\>\& | الصورة التي سيتم إدراجها في المستند. |
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



يظهر كيفية إدراج صورة من كائن إلى مستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::String imageFile = get_ImageDir() + u"Logo.jpg";

// فيما يلي ثلاث طرق لإدراج صورة من نسخة كائن Image.
// 1 -  شكل مضمن بحجم افتراضي يعتمد على أبعاد الصورة الأصلية:
builder->InsertImage(imageFile);

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 2 -  شكل مضمن بأبعاد مخصصة:
builder->InsertImage(imageFile, Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 3 -  شكل عائم بأبعاد مخصصة:
builder->InsertImage(imageFile, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromImageObject.docx");
```

## انظر أيضًا

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::SharedPtr\<System::Drawing::Image\>\&, double, double) method


يقوم بإدراج صورة داخلية من كائن **Image** في المستند ويقوم بتحجيمها إلى الحجم المحدد.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::SharedPtr<System::Drawing::Image> &image, double width, double height)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| image | const System::SharedPtr\<System::Drawing::Image\>\& | الصورة التي سيتم إدراجها في المستند. |
| العرض | double | عرض الصورة بالنقاط. يمكن أن يكون قيمة سالبة أو صفر لطلب مقياس 100٪. |
| الارتفاع | double | ارتفاع الصورة بالنقاط. يمكن أن يكون قيمة سالبة أو صفر لطلب مقياس 100٪. |

### ReturnValue

عقدة الصورة التي تم إدراجها للتو.
## ملاحظات


يمكنك تغيير حجم الصورة، موقعها، طريقة تموضعها وإعدادات أخرى باستخدام كائن [Shape](../../../aspose.words.drawing/shape/) الذي تُعيده هذه الطريقة.

## أمثلة



يظهر كيفية إدراج صورة من كائن إلى مستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::String imageFile = get_ImageDir() + u"Logo.jpg";

// فيما يلي ثلاث طرق لإدراج صورة من نسخة كائن Image.
// 1 -  شكل مضمن بحجم افتراضي يعتمد على أبعاد الصورة الأصلية:
builder->InsertImage(imageFile);

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 2 -  شكل مضمن بأبعاد مخصصة:
builder->InsertImage(imageFile, Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 3 -  شكل عائم بأبعاد مخصصة:
builder->InsertImage(imageFile, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromImageObject.docx");
```

## انظر أيضًا

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::SharedPtr\<System::IO::Stream\>\&) method


يقوم بإدراج صورة من تدفق بيانات في المستند. يتم إدراج الصورة داخل السطر وبنسبة 100٪.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::SharedPtr<System::IO::Stream> &stream)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| تدفق | const System::SharedPtr\<System::IO::Stream\>\& | الدفق الذي يحتوي على الصورة. |

### ReturnValue

عقدة الصورة التي تم إدراجها للتو.
## ملاحظات


يمكنك تغيير حجم الصورة، موقعها، طريقة تموضعها وإعدادات أخرى باستخدام كائن [Shape](../../../aspose.words.drawing/shape/) الذي تُعيده هذه الطريقة.

## أمثلة



يظهر كيفية إدراج صورة من دفق إلى مستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_ImageDir() + u"Logo.jpg");
    // فيما يلي ثلاث طرق لإدراج صورة من دفق.
    // 1 -  شكل مضمن بحجم افتراضي يعتمد على أبعاد الصورة الأصلية:
    builder->InsertImage(stream);

    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

    // 2 -  شكل مضمن بأبعاد مخصصة:
    builder->InsertImage(stream, Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

    // 3 -  شكل عائم بأبعاد مخصصة:
    builder->InsertImage(stream, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);
}

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromStream.docx");
```


يظهر كيفية إدراج شكل مع صورة من دفق إلى مستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_ImageDir() + u"Logo.jpg");
    builder->Write(u"Image from stream: ");
    builder->InsertImage(stream);
}

doc->Save(get_ArtifactsDir() + u"Image.FromStream.docx");
```

## انظر أيضًا

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method


يقوم بإدراج صورة من تدفق بيانات في الموضع والحجم المحددين.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::SharedPtr<System::IO::Stream> &stream, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| تدفق | const System::SharedPtr\<System::IO::Stream\>\& | الدفق الذي يحتوي على الصورة. |
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



يظهر كيفية إدراج صورة من دفق إلى مستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_ImageDir() + u"Logo.jpg");
    // فيما يلي ثلاث طرق لإدراج صورة من دفق.
    // 1 -  شكل مضمن بحجم افتراضي يعتمد على أبعاد الصورة الأصلية:
    builder->InsertImage(stream);

    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

    // 2 -  شكل مضمن بأبعاد مخصصة:
    builder->InsertImage(stream, Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

    // 3 -  شكل عائم بأبعاد مخصصة:
    builder->InsertImage(stream, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);
}

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromStream.docx");
```

## انظر أيضًا

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::SharedPtr\<System::IO::Stream\>\&, double, double) method


يقوم بإدراج صورة داخلية من تدفق بيانات في المستند ويقوم بتحجيمها إلى الحجم المحدد.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::SharedPtr<System::IO::Stream> &stream, double width, double height)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| تدفق | const System::SharedPtr\<System::IO::Stream\>\& | الدفق الذي يحتوي على الصورة. |
| العرض | double | عرض الصورة بالنقاط. يمكن أن يكون قيمة سالبة أو صفر لطلب مقياس 100٪. |
| الارتفاع | double | ارتفاع الصورة بالنقاط. يمكن أن يكون قيمة سالبة أو صفر لطلب مقياس 100٪. |

### ReturnValue

عقدة الصورة التي تم إدراجها للتو.
## ملاحظات


يمكنك تغيير حجم الصورة، موقعها، طريقة تموضعها وإعدادات أخرى باستخدام كائن [Shape](../../../aspose.words.drawing/shape/) الذي تُعيده هذه الطريقة.

## أمثلة



يظهر كيفية إدراج صورة من دفق إلى مستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_ImageDir() + u"Logo.jpg");
    // فيما يلي ثلاث طرق لإدراج صورة من دفق.
    // 1 -  شكل مضمن بحجم افتراضي يعتمد على أبعاد الصورة الأصلية:
    builder->InsertImage(stream);

    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

    // 2 -  شكل مضمن بأبعاد مخصصة:
    builder->InsertImage(stream, Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

    // 3 -  شكل عائم بأبعاد مخصصة:
    builder->InsertImage(stream, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);
}

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromStream.docx");
```

## انظر أيضًا

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::String\&) method


يقوم بإدراج صورة من ملف أو عنوان URL في المستند. يتم إدراج الصورة داخل السطر وبنسبة 100٪.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::String &fileName)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| fileName | const System::String\& | الملف الذي يحتوي على الصورة. يمكن أن يكون أي URI محلي أو بعيد صالح. |

### ReturnValue

عقدة الصورة التي تم إدراجها للتو.
## ملاحظات


سيقوم هذا الإصدار المتعدد بتنزيل الصورة تلقائيًا قبل إدراجها في المستند إذا حددت URI بعيد.

يمكنك تغيير حجم الصورة، موقعها، طريقة تموضعها وإعدادات أخرى باستخدام كائن [Shape](../../../aspose.words.drawing/shape/) الذي تُعيده هذه الطريقة.

## أمثلة



يظهر كيفية إدراج صورة من نظام الملفات المحلي إلى مستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// فيما يلي ثلاث طرق لإدراج صورة من اسم ملف نظام محلي.
// 1 -  شكل مضمن بحجم افتراضي يعتمد على أبعاد الصورة الأصلية:
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 2 -  شكل مضمن بأبعاد مخصصة:
builder->InsertImage(get_ImageDir() + u"Transparent background logo.png", Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 3 -  شكل عائم بأبعاد مخصصة:
builder->InsertImage(get_ImageDir() + u"Windows MetaFile.wmf", Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromFilename.docx");
```


يظهر كيفية تحديد أي صورة سيتم إدراجها.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertImage(get_ImageDir() + u"Scalable Vector Graphics.svg");

// Aspose.Words إدراج صورة SVG إلى المستند كـ PNG مع امتداد svgBlip
// التي تحتوي على تمثيل صورة SVG المتجه الأصلي.
doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertSvgImage.SvgWithSvgBlip.docx");

// Aspose.Words إدراج صورة SVG إلى المستند كـ PNG، تمامًا كما يفعل Microsoft Word للتنسيق القديم.
doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertSvgImage.Svg.doc");

doc->get_CompatibilityOptions()->OptimizeFor(Aspose::Words::Settings::MsWordVersion::Word2003);

// يقوم Aspose.Words بإدراج صورة SVG إلى المستند كملف تعريف بيانات EMF للحفاظ على الصورة في تمثيل متجهي.
doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertSvgImage.Emf.docx");
```


يوضح كيفية إدراج صورة gif إلى المستند.
```cpp
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();

// يمكننا إدراج صورة gif باستخدام المسار أو مصفوفة البايتات.
// يعمل فقط إذا تم تحسين DocumentBuilder إلى إصدار Word 2010 أو أعلى.
// لاحظ أن الوصول إلى بايتات الصورة يسبب تحويل Gif إلى Png.
System::SharedPtr<Aspose::Words::Drawing::Shape> gifImage = builder->InsertImage(get_ImageDir() + u"Graphics Interchange Format.gif");

gifImage = builder->InsertImage(System::IO::File::ReadAllBytes(get_ImageDir() + u"Graphics Interchange Format.gif"));

builder->get_Document()->Save(get_ArtifactsDir() + u"InsertGif.docx");
```


يوضح كيفية إدراج شكل مع صورة في مستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// فيما يلي موقعان حيث يمكن لطريقة "InsertShape" الخاصة بـ document builder
// أن تستمد الصورة التي سيعرضها الشكل.
// 1 -  تمرير اسم ملف صورة من نظام الملفات المحلي:
builder->Write(u"Image from local file: ");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");
builder->Writeln();

// 2 -  تمرير عنوان URL يشير إلى صورة.
builder->Write(u"Image from a URL: ");
builder->InsertImage(get_ImageUrl());
builder->Writeln();

doc->Save(get_ArtifactsDir() + u"Image.FromUrl.docx");
```


يوضح كيفية إدراج صورة عائمة في مركز الصفحة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// أدرج صورة عائمة ستظهر خلف النص المتداخل ووازنها إلى مركز الصفحة.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);
shape->set_BehindText(true);
shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_HorizontalAlignment(Aspose::Words::Drawing::HorizontalAlignment::Center);
shape->set_VerticalAlignment(Aspose::Words::Drawing::VerticalAlignment::Center);

doc->Save(get_ArtifactsDir() + u"Image.CreateFloatingPageCenter.docx");
```


يوضح كيفية إدراج صورة WebP.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertImage(get_ImageDir() + u"WebP image.webp");

doc->Save(get_ArtifactsDir() + u"Image.InsertWebpImage.docx");
```

## انظر أيضًا

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::String\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method


يقوم بإدراج صورة من ملف أو عنوان URL في الموضع والحجم المحددين.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::String &fileName, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| fileName | const System::String\& | الملف الذي يحتوي على الصورة. |
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



يوضح كيفية إدراج صورة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// هناك طريقتان لاستخدام document builder لاستدعاء صورة ثم إدراجها كشكل عائم.
// 1 -  من ملف في نظام الملفات المحلي:
builder->InsertImage(get_ImageDir() + u"Transparent background logo.png", Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 0.0, 200.0, 200.0, Aspose::Words::Drawing::WrapType::Square);

// 2 -  من عنوان URL:
builder->InsertImage(get_ImageUrl(), Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 250.0, 200.0, 200.0, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertFloatingImage.docx");
```


يوضح كيفية إدراج صورة من نظام الملفات المحلي إلى مستند مع الحفاظ على أبعادها.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// تنشئ طريقة InsertImage شكلاً عائمًا مع الصورة الممررة في بيانات الصورة الخاصة به.
// يمكننا تحديد أبعاد الشكل عن طريق تمريرها إلى هذه الطريقة.
System::SharedPtr<Aspose::Words::Drawing::Shape> imageShape = builder->InsertImage(get_ImageDir() + u"Logo.jpg", Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 0.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 0.0, -1.0, -1.0, Aspose::Words::Drawing::WrapType::Square);

// تمرير قيم سلبية كالأبعاد المقصودة سيؤدي تلقائيًا إلى تعريف
// أبعاد الشكل بناءً على أبعاد صورته.
ASPOSE_ASSERT_EQ(300.0, imageShape->get_Width());
ASPOSE_ASSERT_EQ(300.0, imageShape->get_Height());

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertImageOriginalSize.docx");
```


يظهر كيفية إدراج صورة من نظام الملفات المحلي إلى مستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// فيما يلي ثلاث طرق لإدراج صورة من اسم ملف نظام محلي.
// 1 -  شكل مضمن بحجم افتراضي يعتمد على أبعاد الصورة الأصلية:
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 2 -  شكل مضمن بأبعاد مخصصة:
builder->InsertImage(get_ImageDir() + u"Transparent background logo.png", Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 3 -  شكل عائم بأبعاد مخصصة:
builder->InsertImage(get_ImageDir() + u"Windows MetaFile.wmf", Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromFilename.docx");
```

## انظر أيضًا

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::String\&, double, double) method


يقوم بإدراج صورة داخلية من ملف أو عنوان URL في المستند ويقوم بتحجيمها إلى الحجم المحدد.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::String &fileName, double width, double height)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| fileName | const System::String\& | الملف الذي يحتوي على الصورة. |
| العرض | double | عرض الصورة بالنقاط. يمكن أن يكون قيمة سالبة أو صفر لطلب مقياس 100٪. |
| الارتفاع | double | ارتفاع الصورة بالنقاط. يمكن أن يكون قيمة سالبة أو صفر لطلب مقياس 100٪. |

### ReturnValue

عقدة الصورة التي تم إدراجها للتو.
## ملاحظات


يمكنك تغيير حجم الصورة، موقعها، طريقة تموضعها وإعدادات أخرى باستخدام كائن [Shape](../../../aspose.words.drawing/shape/) الذي تُعيده هذه الطريقة.

## أمثلة



يظهر كيفية إدراج صورة من نظام الملفات المحلي إلى مستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// فيما يلي ثلاث طرق لإدراج صورة من اسم ملف نظام محلي.
// 1 -  شكل مضمن بحجم افتراضي يعتمد على أبعاد الصورة الأصلية:
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 2 -  شكل مضمن بأبعاد مخصصة:
builder->InsertImage(get_ImageDir() + u"Transparent background logo.png", Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 3 -  شكل عائم بأبعاد مخصصة:
builder->InsertImage(get_ImageDir() + u"Windows MetaFile.wmf", Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromFilename.docx");
```

## انظر أيضًا

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(std::basic_istream<CharType, Traits> &stream)
```

## انظر أيضًا

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(std::basic_istream\<CharType, Traits\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method




```cpp
template<typename CharType,typename Traits> System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(std::basic_istream<CharType, Traits> &stream, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```

## انظر أيضًا

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(std::basic_istream\<CharType, Traits\>\&, double, double) method




```cpp
template<typename CharType,typename Traits> System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(std::basic_istream<CharType, Traits> &stream, double width, double height)
```

## انظر أيضًا

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
