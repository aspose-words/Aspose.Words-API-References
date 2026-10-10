---
title: "Aspose::Words::LowCode::Comparer::Compare طريقة"
linktitle: "Compare"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::LowCode::Comparer::Compare. يقارن مستندين تم تحميلهما من التدفقات مع خيارات إضافية ويحفظ الاختلافات إلى تدفق الإخراج المقدم بالتنسيق المحدد للحفظ، وينتج التغييرات كعدد من تعديلات التحرير والتنسيق في C++."
type: docs
weight: 1000
url: /ar/cpp/aspose.words.lowcode/comparer/compare/
---
## Comparer::Compare(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime) method


يقارن مستندين تم تحميلهما من تدفقات مع خيارات إضافية ويحفظ الفروقات في تدفق الإخراج المقدم بالتنسيق المحدد للحفظ، منتجًا تغييرات على شكل عدد من تعديلات التحرير والتنسيق.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::SharedPtr<System::IO::Stream> &v1, const System::SharedPtr<System::IO::Stream> &v2, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::String &author, System::DateTime dateTime)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| v1 | const System::SharedPtr\<System::IO::Stream\>\& | المستند الأصلي. |
| v2 | const System::SharedPtr\<System::IO::Stream\>\& | المستند المعدل. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | تدفق الإخراج. |
| saveFormat | Aspose::Words::SaveFormat | تنسيق الحفظ للإخراج. |
| المؤلف | const System::String\& | الأحرف الأولى للمؤلف لاستخدامها في المراجعات. |
| dateTime | System::DateTime | التاريخ والوقت لاستخدامهما في المراجعات. |
## ملاحظات


إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، سيتم حفظ الصفحة الأولى فقط من الإخراج إلى الدفق المحدد.

إذا كان تنسيق الإخراج TIFF، سيتم حفظ الإخراج كملف TIFF متعدد الإطارات واحد إلى الدفق المحدد.

## انظر أيضًا

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) method


يقارن مستندين تم تحميلهما من تدفقات مع خيارات إضافية ويحفظ الفروقات في تدفق الإخراج المقدم بالتنسيق المحدد للحفظ، منتجًا تغييرات على شكل عدد من تعديلات التحرير والتنسيق.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::SharedPtr<System::IO::Stream> &v1, const System::SharedPtr<System::IO::Stream> &v2, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::String &author, System::DateTime dateTime, const System::SharedPtr<Aspose::Words::Comparing::CompareOptions> &compareOptions)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| v1 | const System::SharedPtr\<System::IO::Stream\>\& | المستند الأصلي. |
| v2 | const System::SharedPtr\<System::IO::Stream\>\& | المستند المعدل. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | تدفق الإخراج. |
| saveFormat | Aspose::Words::SaveFormat | تنسيق الحفظ للإخراج. |
| المؤلف | const System::String\& | الأحرف الأولى للمؤلف لاستخدامها في المراجعات. |
| dateTime | System::DateTime | التاريخ والوقت لاستخدامهما في المراجعات. |
| compareOptions | const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\& | خيارات مقارنة [Document](../../../aspose.words/document/). |
## ملاحظات


إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، سيتم حفظ الصفحة الأولى فقط من الإخراج إلى الدفق المحدد.

إذا كان تنسيق الإخراج TIFF، سيتم حفظ الإخراج كملف TIFF متعدد الإطارات واحد إلى الدفق المحدد.

## انظر أيضًا

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, System::DateTime) method


يقارن مستندين تم تحميلهما من تدفقات مع خيارات إضافية ويحفظ الفروقات في تدفق الإخراج المقدم بالتنسيق المحدد للحفظ، منتجًا تغييرات على شكل عدد من تعديلات التحرير والتنسيق.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::SharedPtr<System::IO::Stream> &v1, const System::SharedPtr<System::IO::Stream> &v2, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &author, System::DateTime dateTime)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| v1 | const System::SharedPtr\<System::IO::Stream\>\& | المستند الأصلي. |
| v2 | const System::SharedPtr\<System::IO::Stream\>\& | المستند المعدل. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | تدفق الإخراج. |
| saveOptions | const System::SharedPtr\\<Aspose::Words::Saving::SaveOptions\\>\\& | خيارات الحفظ للإخراج. |
| المؤلف | const System::String\& | الأحرف الأولى للمؤلف لاستخدامها في المراجعات. |
| dateTime | System::DateTime | التاريخ والوقت لاستخدامهما في المراجعات. |
## ملاحظات


إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، سيتم حفظ الصفحة الأولى فقط من الإخراج إلى الدفق المحدد.

إذا كان تنسيق الإخراج TIFF، سيتم حفظ الإخراج كملف TIFF متعدد الإطارات واحد إلى الدفق المحدد.

## انظر أيضًا

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) method


يقارن مستندين تم تحميلهما من تدفقات مع خيارات إضافية ويحفظ الفروقات في تدفق الإخراج المقدم بالتنسيق المحدد للحفظ، منتجًا تغييرات على شكل عدد من تعديلات التحرير والتنسيق.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::SharedPtr<System::IO::Stream> &v1, const System::SharedPtr<System::IO::Stream> &v2, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &author, System::DateTime dateTime, const System::SharedPtr<Aspose::Words::Comparing::CompareOptions> &compareOptions)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| v1 | const System::SharedPtr\<System::IO::Stream\>\& | المستند الأصلي. |
| v2 | const System::SharedPtr\<System::IO::Stream\>\& | المستند المعدل. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | تدفق الإخراج. |
| saveOptions | const System::SharedPtr\\<Aspose::Words::Saving::SaveOptions\\>\\& | خيارات الحفظ للإخراج. |
| المؤلف | const System::String\& | الأحرف الأولى للمؤلف لاستخدامها في المراجعات. |
| dateTime | System::DateTime | التاريخ والوقت لاستخدامهما في المراجعات. |
| compareOptions | const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\& | خيارات مقارنة [Document](../../../aspose.words/document/). |
## ملاحظات


إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، سيتم حفظ الصفحة الأولى فقط من الإخراج إلى الدفق المحدد.

إذا كان تنسيق الإخراج TIFF، سيتم حفظ الإخراج كملف TIFF متعدد الإطارات واحد إلى الدفق المحدد.

## انظر أيضًا

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::String\&, const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime) method


يقارن مستندين مع خيارات إضافية ويحفظ الفروقات في ملف الإخراج المحدد بالتنسيق المحدد للحفظ، منتجًا تغييرات على شكل عدد من تعديلات التحرير والتنسيق.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::String &v1, const System::String &v2, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::String &author, System::DateTime dateTime)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| v1 | const System::String\& | المستند الأصلي. |
| v2 | const System::String\& | المستند المعدل. |
| outputFileName | const System::String\& | اسم ملف الإخراج. |
| saveFormat | Aspose::Words::SaveFormat | تنسيق الحفظ للإخراج. |
| المؤلف | const System::String\& | الأحرف الأولى للمؤلف لاستخدامها في المراجعات. |
| dateTime | System::DateTime | التاريخ والوقت لاستخدامهما في المراجعات. |
## ملاحظات


إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، سيتم حفظ كل صفحة من الإخراج كملف منفصل. سيُستخدم اسم ملف الإخراج المحدد لتوليد أسماء الملفات لكل جزء وفق القاعدة: outputFile_partIndex.extension.

إذا كان تنسيق الإخراج TIFF، سيتم حفظ الإخراج كملف TIFF متعدد الإطارات واحد.

## انظر أيضًا

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::String\&, const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) method


يقارن مستندين مع خيارات إضافية ويحفظ الفروقات في ملف الإخراج المحدد بالتنسيق المحدد للحفظ، منتجًا تغييرات على شكل عدد من تعديلات التحرير والتنسيق.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::String &v1, const System::String &v2, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::String &author, System::DateTime dateTime, const System::SharedPtr<Aspose::Words::Comparing::CompareOptions> &compareOptions)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| v1 | const System::String\& | المستند الأصلي. |
| v2 | const System::String\& | المستند المعدل. |
| outputFileName | const System::String\& | اسم ملف الإخراج. |
| saveFormat | Aspose::Words::SaveFormat | تنسيق الحفظ للإخراج. |
| المؤلف | const System::String\& | الأحرف الأولى للمؤلف لاستخدامها في المراجعات. |
| dateTime | System::DateTime | التاريخ والوقت لاستخدامهما في المراجعات. |
| compareOptions | const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\& | خيارات مقارنة [Document](../../../aspose.words/document/). |
## ملاحظات


إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، سيتم حفظ كل صفحة من الإخراج كملف منفصل. سيُستخدم اسم ملف الإخراج المحدد لتوليد أسماء الملفات لكل جزء وفق القاعدة: outputFile_partIndex.extension.

إذا كان تنسيق الإخراج TIFF، سيتم حفظ الإخراج كملف TIFF متعدد الإطارات واحد.

## انظر أيضًا

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::String\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, System::DateTime) method


يقارن مستندين مع خيارات إضافية ويحفظ الفروقات في ملف الإخراج المحدد بالتنسيق المحدد للحفظ، منتجًا تغييرات على شكل عدد من تعديلات التحرير والتنسيق.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::String &v1, const System::String &v2, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &author, System::DateTime dateTime)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| v1 | const System::String\& | المستند الأصلي. |
| v2 | const System::String\& | المستند المعدل. |
| outputFileName | const System::String\& | اسم ملف الإخراج. |
| saveOptions | const System::SharedPtr\\<Aspose::Words::Saving::SaveOptions\\>\\& | خيارات الحفظ للإخراج. |
| المؤلف | const System::String\& | الأحرف الأولى للمؤلف لاستخدامها في المراجعات. |
| dateTime | System::DateTime | التاريخ والوقت لاستخدامهما في المراجعات. |
## ملاحظات


إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، سيتم حفظ كل صفحة من الإخراج كملف منفصل. سيُستخدم اسم ملف الإخراج المحدد لتوليد أسماء الملفات لكل جزء وفق القاعدة: outputFile_partIndex.extension.

إذا كان تنسيق الإخراج TIFF، سيتم حفظ الإخراج كملف TIFF متعدد الإطارات واحد.

## انظر أيضًا

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::String\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) method


يقارن مستندين مع خيارات إضافية ويحفظ الفروقات في ملف الإخراج المحدد بالتنسيق المحدد للحفظ، منتجًا تغييرات على شكل عدد من تعديلات التحرير والتنسيق.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::String &v1, const System::String &v2, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &author, System::DateTime dateTime, const System::SharedPtr<Aspose::Words::Comparing::CompareOptions> &compareOptions)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| v1 | const System::String\& | المستند الأصلي. |
| v2 | const System::String\& | المستند المعدل. |
| outputFileName | const System::String\& | اسم ملف الإخراج. |
| saveOptions | const System::SharedPtr\\<Aspose::Words::Saving::SaveOptions\\>\\& | خيارات الحفظ للإخراج. |
| المؤلف | const System::String\& | الأحرف الأولى للمؤلف لاستخدامها في المراجعات. |
| dateTime | System::DateTime | التاريخ والوقت لاستخدامهما في المراجعات. |
| compareOptions | const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\& | خيارات مقارنة [Document](../../../aspose.words/document/). |
## ملاحظات


إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، سيتم حفظ كل صفحة من الإخراج كملف منفصل. سيُستخدم اسم ملف الإخراج المحدد لتوليد أسماء الملفات لكل جزء وفق القاعدة: outputFile_partIndex.extension.

إذا كان تنسيق الإخراج TIFF، سيتم حفظ الإخراج كملف TIFF متعدد الإطارات واحد.

## انظر أيضًا

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::String\&, const System::String\&, const System::String\&, const System::String\&, System::DateTime) method


يقارن مستندين مع خيارات إضافية ويحفظ الفروقات في ملف الإخراج المحدد، منتجًا تغييرات على شكل عدد من تعديلات التحرير والتنسيق.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::String &v1, const System::String &v2, const System::String &outputFileName, const System::String &author, System::DateTime dateTime)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| v1 | const System::String\& | المستند الأصلي. |
| v2 | const System::String\& | المستند المعدل. |
| outputFileName | const System::String\& | اسم ملف الإخراج. |
| المؤلف | const System::String\& | الأحرف الأولى للمؤلف لاستخدامها في المراجعات. |
| dateTime | System::DateTime | التاريخ والوقت لاستخدامهما في المراجعات. |
## ملاحظات


إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، سيتم حفظ كل صفحة من الإخراج كملف منفصل. سيُستخدم اسم ملف الإخراج المحدد لتوليد أسماء الملفات لكل جزء وفق القاعدة: outputFile_partIndex.extension.

إذا كان تنسيق الإخراج TIFF، سيتم حفظ الإخراج كملف TIFF متعدد الإطارات واحد.

## انظر أيضًا

* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::String\&, const System::String\&, const System::String\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) method


يقارن مستندين مع خيارات إضافية ويحفظ الفروقات في ملف الإخراج المحدد، منتجًا تغييرات على شكل عدد من تعديلات التحرير والتنسيق.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::String &v1, const System::String &v2, const System::String &outputFileName, const System::String &author, System::DateTime dateTime, const System::SharedPtr<Aspose::Words::Comparing::CompareOptions> &compareOptions)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| v1 | const System::String\& | المستند الأصلي. |
| v2 | const System::String\& | المستند المعدل. |
| outputFileName | const System::String\& | اسم ملف الإخراج. |
| المؤلف | const System::String\& | الأحرف الأولى للمؤلف لاستخدامها في المراجعات. |
| dateTime | System::DateTime | التاريخ والوقت لاستخدامهما في المراجعات. |
| compareOptions | const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\& | خيارات مقارنة [Document](../../../aspose.words/document/). |
## ملاحظات


إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، سيتم حفظ كل صفحة من الإخراج كملف منفصل. سيُستخدم اسم ملف الإخراج المحدد لتوليد أسماء الملفات لكل جزء وفق القاعدة: outputFile_partIndex.extension.

إذا كان تنسيق الإخراج TIFF، سيتم حفظ الإخراج كملف TIFF متعدد الإطارات واحد.

## انظر أيضًا

* Class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
