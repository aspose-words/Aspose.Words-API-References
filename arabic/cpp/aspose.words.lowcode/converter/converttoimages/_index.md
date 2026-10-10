---
title: "طريقة Aspose::Words::LowCode::Converter::ConvertToImages"
linktitle: "ConvertToImages"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::LowCode::Converter::ConvertToImages. يحول صفحات المستند المحدد إلى صور بالتنسيق المحدد ويعيد مصفوفة من التدفقات التي تحتوي على الصور في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.lowcode/converter/converttoimages/
---
## Converter::ConvertToImages(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::SaveFormat) method


يقوم بتحويل صفحات المستند المحدد إلى صور بالتنسيق المحدد ويعيد مصفوفة من التدفقات التي تحتوي على الصور.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Converter::ConvertToImages(const System::SharedPtr<Aspose::Words::Document> &doc, Aspose::Words::SaveFormat saveFormat)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::Document\>\& | المستند الإدخالي. |
| saveFormat | Aspose::Words::SaveFormat | تنسيق الحفظ. يُسمح فقط بتنسيقات حفظ الصور. |

### ReturnValue

يعيد مصفوفة من تدفقات الصور. يجب على المستخدم النهائي التخلص من التدفقات.

## انظر أيضًا

* Class [Document](../../../aspose.words/document/)
* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::SharedPtr\<Aspose::Words::Document\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) method


يقوم بتحويل صفحات المستند المحدد إلى صور باستخدام خيارات الحفظ المحددة ويعيد مصفوفة من التدفقات التي تحتوي على الصور.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Converter::ConvertToImages(const System::SharedPtr<Aspose::Words::Document> &doc, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::Document\>\& | المستند الإدخالي. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | خيارات حفظ الصورة. |

### ReturnValue

يعيد مصفوفة من تدفقات الصور. يجب على المستخدم النهائي التخلص من التدفقات.

## انظر أيضًا

* Class [Document](../../../aspose.words/document/)
* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) method


يقوم بتحويل صفحات تدفق الإدخال المحدد إلى صور بالتنسيق المحدد ويعيد مصفوفة من التدفقات التي تحتوي على الصور.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Converter::ConvertToImages(const System::SharedPtr<System::IO::Stream> &inputStream, Aspose::Words::SaveFormat saveFormat)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | دفق الإدخال. |
| saveFormat | Aspose::Words::SaveFormat | تنسيق الحفظ. يُسمح فقط بتنسيقات حفظ الصور. |

### ReturnValue

يعيد مصفوفة من تدفقات الصور. يجب على المستخدم النهائي التخلص من التدفقات.

## انظر أيضًا

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) method


يقوم بتحويل صفحات تدفق الإدخال المحدد إلى صور باستخدام خيارات التحميل والحفظ المقدمة، ويعيد مصفوفة من التدفقات التي تحتوي على الصور.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Converter::ConvertToImages(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> &loadOptions, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | دفق الإدخال. |
| loadOptions | const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\& | خيارات تحميل المستند الإدخالي. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | خيارات حفظ الصورة. |

### ReturnValue

يعيد مصفوفة من تدفقات الصور. يجب على المستخدم النهائي التخلص من التدفقات.

## انظر أيضًا

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) method


يقوم بتحويل صفحات تدفق الإدخال المحدد إلى صور باستخدام خيارات الحفظ المحددة ويعيد مصفوفة من التدفقات التي تحتوي على الصور.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Converter::ConvertToImages(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | دفق الإدخال. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | خيارات حفظ الصورة. |

### ReturnValue

يعيد مصفوفة من تدفقات الصور. يجب على المستخدم النهائي التخلص من التدفقات.

## انظر أيضًا

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::String\&, Aspose::Words::SaveFormat) method


يقوم بتحويل صفحات ملف الإدخال المحدد إلى صور بالتنسيق المحدد ويعيد مصفوفة من التدفقات التي تحتوي على الصور.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Converter::ConvertToImages(const System::String &inputFile, Aspose::Words::SaveFormat saveFormat)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| inputFile | const System::String\& | اسم ملف الإدخال. |
| saveFormat | Aspose::Words::SaveFormat | تنسيق الحفظ. يُسمح فقط بتنسيقات حفظ الصور. |

### ReturnValue

يعيد مصفوفة من تدفقات الصور. يجب على المستخدم النهائي التخلص من التدفقات.

## انظر أيضًا

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) method


يقوم بتحويل صفحات ملف الإدخال المحدد إلى ملفات صورة باستخدام خيارات التحميل والحفظ المقدمة.

```cpp
static void Aspose::Words::LowCode::Converter::ConvertToImages(const System::String &inputFile, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> &loadOptions, const System::String &outputFile, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| inputFile | const System::String\& | اسم ملف الإدخال. |
| loadOptions | const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\& | خيارات تحميل المستند الإدخالي. |
| outputFile | const System::String\& | اسم ملف الإخراج المستخدم لإنشاء اسم ملف لصور الصفحات باستخدام القاعدة "outputFile_pageIndex.extension". |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | خيارات حفظ الصورة. |

## انظر أيضًا

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) method


يقوم بتحويل صفحات ملف الإدخال المحدد إلى صور باستخدام خيارات الحفظ المحددة ويعيد مصفوفة من التدفقات التي تحتوي على الصور.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Converter::ConvertToImages(const System::String &inputFile, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| inputFile | const System::String\& | اسم ملف الإدخال. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | خيارات حفظ الصورة. |

### ReturnValue

يعيد مصفوفة من تدفقات الصور. يجب على المستخدم النهائي التخلص من التدفقات.

## انظر أيضًا

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::String\&, const System::String\&) method


يقوم بتحويل صفحات ملف الإدخال المحدد إلى ملفات صورة.

```cpp
static void Aspose::Words::LowCode::Converter::ConvertToImages(const System::String &inputFile, const System::String &outputFile)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| inputFile | const System::String\& | اسم ملف الإدخال. |
| outputFile | const System::String\& | اسم ملف الإخراج المستخدم لإنشاء اسم ملف لصور الصفحات باستخدام القاعدة "outputFile_pageIndex.extension". |

## انظر أيضًا

* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::String\&, const System::String\&, Aspose::Words::SaveFormat) method


يقوم بتحويل صفحات ملف الإدخال المحدد إلى ملفات صورة بالتنسيق المحدد.

```cpp
static void Aspose::Words::LowCode::Converter::ConvertToImages(const System::String &inputFile, const System::String &outputFile, Aspose::Words::SaveFormat saveFormat)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| inputFile | const System::String\& | اسم ملف الإدخال. |
| outputFile | const System::String\& | اسم ملف الإخراج المستخدم لإنشاء اسم ملف لصور الصفحات باستخدام القاعدة "outputFile_pageIndex.extension". |
| saveFormat | Aspose::Words::SaveFormat | تنسيق الحفظ. يُسمح فقط بتنسيقات حفظ الصور. |

## انظر أيضًا

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) method


يقوم بتحويل صفحات ملف الإدخال المحدد إلى ملفات صورة باستخدام خيارات الحفظ المحددة.

```cpp
static void Aspose::Words::LowCode::Converter::ConvertToImages(const System::String &inputFile, const System::String &outputFile, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| inputFile | const System::String\& | اسم ملف الإدخال. |
| outputFile | const System::String\& | اسم ملف الإخراج المستخدم لإنشاء اسم ملف لصور الصفحات باستخدام القاعدة "outputFile_pageIndex.extension". |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | خيارات حفظ الصورة. |

## انظر أيضًا

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
