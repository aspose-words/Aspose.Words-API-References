---
title: "Aspose::Words::LowCode::Converter::Convert طريقة"
linktitle: "تحويل"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::LowCode::Converter::Convert. يحول المستند الإدخالي المعطى إلى مستند إخراج واحد باستخدام تدفقات الإدخال والإخراج المحددة في C++."
type: docs
weight: 1000
url: /ar/cpp/aspose.words.lowcode/converter/convert/
---
## Converter::Convert(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) method


يقوم بتحويل المستند الإدخالي المعطى إلى مستند إخراجي واحد باستخدام تدفقات الإدخال والإخراج المحددة.

```cpp
static void Aspose::Words::LowCode::Converter::Convert(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> &loadOptions, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | تدفقات الإدخال. |
| loadOptions | const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\& | خيارات تحميل المستند الإدخالي. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | تدفق الإخراج. |
| saveOptions | const System::SharedPtr\\<Aspose::Words::Saving::SaveOptions\\>\\& | خيارات الحفظ. |
## ملاحظات


إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، سيتم حفظ الصفحة الأولى فقط من الإخراج إلى الدفق المحدد.

إذا كان تنسيق الإخراج TIFF، سيتم حفظ الإخراج كملف TIFF متعدد الإطارات واحد إلى الدفق المحدد.

## انظر أيضًا

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::Convert(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) method


يقوم بتحويل المستند الإدخالي المعطى إلى مستند إخراجي واحد باستخدام تدفقات الإدخال والإخراج المحددة.

```cpp
static void Aspose::Words::LowCode::Converter::Convert(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | دفق الإدخال. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | تدفق الإخراج. |
| saveFormat | Aspose::Words::SaveFormat | تنسيق الحفظ. |
## ملاحظات


إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، سيتم حفظ الصفحة الأولى فقط من الإخراج إلى الدفق المحدد.

إذا كان تنسيق الإخراج TIFF، سيتم حفظ الإخراج كملف TIFF متعدد الإطارات واحد إلى الدفق المحدد.

## انظر أيضًا

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::Convert(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) method


يقوم بتحويل المستند الإدخالي المعطى إلى مستند إخراجي واحد باستخدام تدفقات الإدخال والإخراج المحددة.

```cpp
static void Aspose::Words::LowCode::Converter::Convert(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | تدفقات الإدخال. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | تدفق الإخراج. |
| saveOptions | const System::SharedPtr\\<Aspose::Words::Saving::SaveOptions\\>\\& | خيارات الحفظ. |
## ملاحظات


إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، سيتم حفظ الصفحة الأولى فقط من الإخراج إلى الدفق المحدد.

إذا كان تنسيق الإخراج TIFF، سيتم حفظ الإخراج كملف TIFF متعدد الإطارات واحد إلى الدفق المحدد.

## انظر أيضًا

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::Convert(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) method


يقوم بتحويل المستند الإدخالي المعطى إلى المستند الإخراجي باستخدام أسماء ملفات الإدخال والإخراج المحددة وخيارات التحميل/الحفظ الخاصة به.

```cpp
static void Aspose::Words::LowCode::Converter::Convert(const System::String &inputFile, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> &loadOptions, const System::String &outputFile, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| inputFile | const System::String\& | اسم ملف الإدخال. |
| loadOptions | const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\& | خيارات تحميل المستند الإدخالي. |
| outputFile | const System::String\& | اسم ملف الإخراج. |
| saveOptions | const System::SharedPtr\\<Aspose::Words::Saving::SaveOptions\\>\\& | خيارات الحفظ. |
## ملاحظات


إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، سيتم حفظ كل صفحة من الإخراج كملف منفصل. سيُستخدم اسم ملف الإخراج المحدد لتوليد أسماء الملفات لكل جزء وفق القاعدة: outputFile_partIndex.extension.

إذا كان تنسيق الإخراج TIFF، سيتم حفظ الإخراج كملف TIFF متعدد الإطارات واحد.

## انظر أيضًا

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::Convert(const System::String\&, const System::String\&) method


يحوِّل المستند المدخل المحدد إلى المستند الناتج باستخدام أسماء ملفات الإدخال والإخراج المحددة وامتداداتها.

```cpp
static void Aspose::Words::LowCode::Converter::Convert(const System::String &inputFile, const System::String &outputFile)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| inputFile | const System::String\& | اسم ملف الإدخال. |
| outputFile | const System::String\& | اسم ملف الإخراج. |
## ملاحظات


إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، سيتم حفظ كل صفحة من الإخراج كملف منفصل. سيُستخدم اسم ملف الإخراج المحدد لتوليد أسماء الملفات لكل جزء وفق القاعدة: outputFile_partIndex.extension.

إذا كان تنسيق الإخراج TIFF، سيتم حفظ الإخراج كملف TIFF متعدد الإطارات واحد.

## انظر أيضًا

* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::Convert(const System::String\&, const System::String\&, Aspose::Words::SaveFormat) method


يقوم بتحويل المستند الإدخالي المعطى إلى المستند الإخراجي باستخدام أسماء ملفات الإدخال والإخراج المحددة وتنسيق المستند النهائي.

```cpp
static void Aspose::Words::LowCode::Converter::Convert(const System::String &inputFile, const System::String &outputFile, Aspose::Words::SaveFormat saveFormat)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| inputFile | const System::String\& | اسم ملف الإدخال. |
| outputFile | const System::String\& | اسم ملف الإخراج. |
| saveFormat | Aspose::Words::SaveFormat | تنسيق الحفظ. |
## ملاحظات


إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، سيتم حفظ كل صفحة من الإخراج كملف منفصل. سيُستخدم اسم ملف الإخراج المحدد لتوليد أسماء الملفات لكل جزء وفق القاعدة: outputFile_partIndex.extension.

إذا كان تنسيق الإخراج TIFF، سيتم حفظ الإخراج كملف TIFF متعدد الإطارات واحد.

## انظر أيضًا

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::Convert(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) method


يقوم بتحويل المستند الإدخالي المعطى إلى المستند الإخراجي باستخدام أسماء ملفات الإدخال والإخراج المحددة وخيارات الحفظ.

```cpp
static void Aspose::Words::LowCode::Converter::Convert(const System::String &inputFile, const System::String &outputFile, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| inputFile | const System::String\& | اسم ملف الإدخال. |
| outputFile | const System::String\& | اسم ملف الإخراج. |
| saveOptions | const System::SharedPtr\\<Aspose::Words::Saving::SaveOptions\\>\\& | خيارات الحفظ. |
## ملاحظات


إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، سيتم حفظ كل صفحة من الإخراج كملف منفصل. سيُستخدم اسم ملف الإخراج المحدد لتوليد أسماء الملفات لكل جزء وفق القاعدة: outputFile_partIndex.extension.

إذا كان تنسيق الإخراج TIFF، سيتم حفظ الإخراج كملف TIFF متعدد الإطارات واحد.

## انظر أيضًا

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
