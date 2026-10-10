---
title: "Aspose::Words::LowCode::Splitter::ExtractPages طريقة"
linktitle: "ExtractPages"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::LowCode::Splitter::ExtractPages طريقة. يستخرج نطاقًا محددًا من الصفحات من تدفق المستند ويحفظ الصفحات المستخرجة إلى تدفق إخراج باستخدام تنسيق الحفظ المحدد في C++."
type: docs
weight: 1000
url: /ar/cpp/aspose.words.lowcode/splitter/extractpages/
---
## Splitter::ExtractPages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, int32_t, int32_t) method


يستخرج نطاقًا محددًا من الصفحات من تدفق المستند ويحفظ الصفحات المستخرجة إلى تدفق إخراج باستخدام تنسيق الحفظ المحدد.

```cpp
static void Aspose::Words::LowCode::Splitter::ExtractPages(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, int32_t startPageIndex, int32_t pageCount)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | دفق الإدخال. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | تدفق الإخراج. |
| saveFormat | Aspose::Words::SaveFormat | تنسيق الحفظ. |
| startPageIndex | int32_t | الفهرس الصفري للصفحة الأولى التي سيتم استخراجها. |
| pageCount | int32_t | عدد الصفحات التي سيتم استخراجها. |

## انظر أيضًا

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::ExtractPages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, int32_t, int32_t) method


يستخرج نطاقًا محددًا من الصفحات من تدفق المستند ويحفظ الصفحات المستخرجة إلى تدفق إخراج باستخدام تنسيق الحفظ المحدد.

```cpp
static void Aspose::Words::LowCode::Splitter::ExtractPages(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, int32_t startPageIndex, int32_t pageCount)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | دفق الإدخال. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | تدفق الإخراج. |
| saveOptions | const System::SharedPtr\\<Aspose::Words::Saving::SaveOptions\\>\\& | خيارات الحفظ. |
| startPageIndex | int32_t | الفهرس الصفري للصفحة الأولى التي سيتم استخراجها. |
| pageCount | int32_t | عدد الصفحات التي سيتم استخراجها. |

## انظر أيضًا

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::ExtractPages(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, int32_t, int32_t) method


يستخرج نطاقًا محددًا من الصفحات من ملف مستند ويحفظ الصفحات المستخرجة في ملف جديد باستخدام تنسيق الحفظ المحدد.

```cpp
static void Aspose::Words::LowCode::Splitter::ExtractPages(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, int32_t startPageIndex, int32_t pageCount)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| inputFileName | const System::String\& | اسم ملف الإدخال. |
| outputFileName | const System::String\& | اسم ملف الإخراج. |
| saveFormat | Aspose::Words::SaveFormat | تنسيق الحفظ. |
| startPageIndex | int32_t | الفهرس الصفري للصفحة الأولى التي سيتم استخراجها. |
| pageCount | int32_t | عدد الصفحات التي سيتم استخراجها. |

## انظر أيضًا

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::ExtractPages(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, int32_t, int32_t) method


يستخرج نطاقًا محددًا من الصفحات من ملف مستند ويحفظ الصفحات المستخرجة في ملف جديد باستخدام تنسيق الحفظ المحدد.

```cpp
static void Aspose::Words::LowCode::Splitter::ExtractPages(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, int32_t startPageIndex, int32_t pageCount)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| inputFileName | const System::String\& | اسم ملف الإدخال. |
| outputFileName | const System::String\& | اسم ملف الإخراج. |
| saveOptions | const System::SharedPtr\\<Aspose::Words::Saving::SaveOptions\\>\\& | خيارات الحفظ. |
| startPageIndex | int32_t | الفهرس الصفري للصفحة الأولى التي سيتم استخراجها. |
| pageCount | int32_t | عدد الصفحات التي سيتم استخراجها. |

## انظر أيضًا

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::ExtractPages(const System::String\&, const System::String\&, int32_t, int32_t) method


يستخرج نطاقًا محددًا من الصفحات من ملف مستند ويحفظ الصفحات المستخرجة في ملف جديد. يتم تحديد تنسيق ملف الإخراج بناءً على امتداد اسم ملف الإخراج.

```cpp
static void Aspose::Words::LowCode::Splitter::ExtractPages(const System::String &inputFileName, const System::String &outputFileName, int32_t startPageIndex, int32_t pageCount)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| inputFileName | const System::String\& | اسم ملف الإدخال. |
| outputFileName | const System::String\& | اسم ملف الإخراج. |
| startPageIndex | int32_t | الفهرس الصفري للصفحة الأولى التي سيتم استخراجها. |
| pageCount | int32_t | عدد الصفحات التي سيتم استخراجها. |

## انظر أيضًا

* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
