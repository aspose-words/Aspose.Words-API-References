---
title: "Aspose::Words::LowCode::Watermarker::SetText طريقة"
linktitle: "SetText"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::LowCode::Watermarker::SetText طريقة. يضيف علامة مائية نصية إلى المستند من التدفقات مع خيارات في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.lowcode/watermarker/settext/
---
## Watermarker::SetText(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&) method


يضيف علامة مائية نصية إلى المستند من التدفقات مع خيارات.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetText(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::String &watermarkText)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | دفق الإدخال. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | تدفق الإخراج. |
| saveFormat | Aspose::Words::SaveFormat | تنسيق الحفظ. |
| watermarkText | const System::String\& | النص المعروض كعلامة مائية. |
## ملاحظات


إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، سيتم حفظ الصفحة الأولى فقط من الإخراج إلى الدفق المحدد.

إذا كان تنسيق الإخراج TIFF، سيتم حفظ الإخراج كملف TIFF متعدد الإطارات واحد إلى الدفق المحدد.

## انظر أيضًا

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetText(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) method


يضيف علامة مائية نصية إلى المستند من التدفقات مع خيارات.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetText(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::String &watermarkText, const System::SharedPtr<Aspose::Words::TextWatermarkOptions> &options)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | دفق الإدخال. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | تدفق الإخراج. |
| saveFormat | Aspose::Words::SaveFormat | تنسيق الحفظ. |
| watermarkText | const System::String\& | النص المعروض كعلامة مائية. |
| خيارات | const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\& | يحدد خيارات إضافية للعلامة المائية النصية. |
## ملاحظات


إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، سيتم حفظ الصفحة الأولى فقط من الإخراج إلى الدفق المحدد.

إذا كان تنسيق الإخراج TIFF، سيتم حفظ الإخراج كملف TIFF متعدد الإطارات واحد إلى الدفق المحدد.

## انظر أيضًا

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetText(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&) method


يضيف علامة مائية نصية إلى المستند من التدفقات مع خيارات.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetText(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &watermarkText)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | دفق الإدخال. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | تدفق الإخراج. |
| saveOptions | const System::SharedPtr\\<Aspose::Words::Saving::SaveOptions\\>\\& | خيارات الحفظ. |
| watermarkText | const System::String\& | النص المعروض كعلامة مائية. |
## ملاحظات


إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، سيتم حفظ الصفحة الأولى فقط من الإخراج إلى الدفق المحدد.

إذا كان تنسيق الإخراج TIFF، سيتم حفظ الإخراج كملف TIFF متعدد الإطارات واحد إلى الدفق المحدد.

## انظر أيضًا

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetText(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) method


يضيف علامة مائية نصية إلى المستند من التدفقات مع خيارات.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetText(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &watermarkText, const System::SharedPtr<Aspose::Words::TextWatermarkOptions> &options)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | دفق الإدخال. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | تدفق الإخراج. |
| saveOptions | const System::SharedPtr\\<Aspose::Words::Saving::SaveOptions\\>\\& | خيارات الحفظ. |
| watermarkText | const System::String\& | النص المعروض كعلامة مائية. |
| خيارات | const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\& | يحدد خيارات إضافية للعلامة المائية النصية. |
## ملاحظات


إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، سيتم حفظ الصفحة الأولى فقط من الإخراج إلى الدفق المحدد.

إذا كان تنسيق الإخراج TIFF، سيتم حفظ الإخراج كملف TIFF متعدد الإطارات واحد إلى الدفق المحدد.

## انظر أيضًا

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetText(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&) method


يضيف علامة مائية نصية إلى المستند مع خيارات وتنسيق حفظ محدد.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetText(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::String &watermarkText)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| inputFileName | const System::String\& | اسم ملف الإدخال. |
| outputFileName | const System::String\& | اسم ملف الإخراج. |
| saveFormat | Aspose::Words::SaveFormat | تنسيق الحفظ. |
| watermarkText | const System::String\& | النص المعروض كعلامة مائية. |
## ملاحظات


إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، سيتم حفظ كل صفحة من الإخراج كملف منفصل. سيُستخدم اسم ملف الإخراج المحدد لتوليد أسماء الملفات لكل جزء وفق القاعدة: outputFile_partIndex.extension.

إذا كان تنسيق الإخراج TIFF، سيتم حفظ الإخراج كملف TIFF متعدد الإطارات واحد.

## انظر أيضًا

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetText(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) method


يضيف علامة مائية نصية إلى المستند مع خيارات وتنسيق حفظ محدد.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetText(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::String &watermarkText, const System::SharedPtr<Aspose::Words::TextWatermarkOptions> &options)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| inputFileName | const System::String\& | اسم ملف الإدخال. |
| outputFileName | const System::String\& | اسم ملف الإخراج. |
| saveFormat | Aspose::Words::SaveFormat | تنسيق الحفظ. |
| watermarkText | const System::String\& | النص المعروض كعلامة مائية. |
| خيارات | const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\& | يحدد خيارات إضافية للعلامة المائية النصية. |
## ملاحظات


إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، سيتم حفظ كل صفحة من الإخراج كملف منفصل. سيُستخدم اسم ملف الإخراج المحدد لتوليد أسماء الملفات لكل جزء وفق القاعدة: outputFile_partIndex.extension.

إذا كان تنسيق الإخراج TIFF، سيتم حفظ الإخراج كملف TIFF متعدد الإطارات واحد.

## انظر أيضًا

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetText(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&) method


يضيف علامة مائية نصية إلى المستند مع خيارات وتنسيق حفظ محدد.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetText(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &watermarkText)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| inputFileName | const System::String\& | اسم ملف الإدخال. |
| outputFileName | const System::String\& | اسم ملف الإخراج. |
| saveOptions | const System::SharedPtr\\<Aspose::Words::Saving::SaveOptions\\>\\& | خيارات الحفظ. |
| watermarkText | const System::String\& | النص المعروض كعلامة مائية. |
## ملاحظات


إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، سيتم حفظ كل صفحة من الإخراج كملف منفصل. سيُستخدم اسم ملف الإخراج المحدد لتوليد أسماء الملفات لكل جزء وفق القاعدة: outputFile_partIndex.extension.

إذا كان تنسيق الإخراج TIFF، سيتم حفظ الإخراج كملف TIFF متعدد الإطارات واحد.

## انظر أيضًا

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetText(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) method


يضيف علامة مائية نصية إلى المستند مع خيارات وتنسيق حفظ محدد.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetText(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &watermarkText, const System::SharedPtr<Aspose::Words::TextWatermarkOptions> &options)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| inputFileName | const System::String\& | اسم ملف الإدخال. |
| outputFileName | const System::String\& | اسم ملف الإخراج. |
| saveOptions | const System::SharedPtr\\<Aspose::Words::Saving::SaveOptions\\>\\& | خيارات الحفظ. |
| watermarkText | const System::String\& | النص المعروض كعلامة مائية. |
| خيارات | const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\& | يحدد خيارات إضافية للعلامة المائية النصية. |
## ملاحظات


إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، سيتم حفظ كل صفحة من الإخراج كملف منفصل. سيُستخدم اسم ملف الإخراج المحدد لتوليد أسماء الملفات لكل جزء وفق القاعدة: outputFile_partIndex.extension.

إذا كان تنسيق الإخراج TIFF، سيتم حفظ الإخراج كملف TIFF متعدد الإطارات واحد.

## انظر أيضًا

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetText(const System::String\&, const System::String\&, const System::String\&) method


يضيف علامة مائية نصية إلى المستند.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetText(const System::String &inputFileName, const System::String &outputFileName, const System::String &watermarkText)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| inputFileName | const System::String\& | اسم ملف الإدخال. |
| outputFileName | const System::String\& | اسم ملف الإخراج. |
| watermarkText | const System::String\& | النص المعروض كعلامة مائية. |
## ملاحظات


إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، سيتم حفظ كل صفحة من الإخراج كملف منفصل. سيُستخدم اسم ملف الإخراج المحدد لتوليد أسماء الملفات لكل جزء وفق القاعدة: outputFile_partIndex.extension.

إذا كان تنسيق الإخراج TIFF، سيتم حفظ الإخراج كملف TIFF متعدد الإطارات واحد.

## انظر أيضًا

* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetText(const System::String\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) method


يضيف علامة مائية نصية إلى المستند مع خيارات.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetText(const System::String &inputFileName, const System::String &outputFileName, const System::String &watermarkText, const System::SharedPtr<Aspose::Words::TextWatermarkOptions> &options)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| inputFileName | const System::String\& | اسم ملف الإدخال. |
| outputFileName | const System::String\& | اسم ملف الإخراج. |
| watermarkText | const System::String\& | النص المعروض كعلامة مائية. |
| خيارات | const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\& | يحدد خيارات إضافية للعلامة المائية النصية. |
## ملاحظات


إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، سيتم حفظ كل صفحة من الإخراج كملف منفصل. سيُستخدم اسم ملف الإخراج المحدد لتوليد أسماء الملفات لكل جزء وفق القاعدة: outputFile_partIndex.extension.

إذا كان تنسيق الإخراج TIFF، سيتم حفظ الإخراج كملف TIFF متعدد الإطارات واحد.

## انظر أيضًا

* Class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
