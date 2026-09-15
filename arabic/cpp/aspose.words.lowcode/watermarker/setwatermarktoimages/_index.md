---
title: "Aspose::Words::LowCode::Watermarker::SetWatermarkToImages طريقة"
linktitle: "SetWatermarkToImages"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::LowCode::Watermarker::SetWatermarkToImages. يضيف علامة مائية صورة إلى المستند مع خيارات. يحول الإخراج إلى صور في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.lowcode/watermarker/setwatermarktoimages/
---
## Watermarker::SetWatermarkToImages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::SharedPtr\<System::IO::Stream\>\&) method


يضيف علامة مائية صورة إلى المستند مع خيارات. يُولِّد المخرجات كصور.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Watermarker::SetWatermarkToImages(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions, const System::SharedPtr<System::IO::Stream> &watermarkImageStream)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | دفق الإدخال. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | خيارات الحفظ. |
| watermarkImageStream | const System::SharedPtr\<System::IO::Stream\>\& | تدفق الصورة المعروض كعلامة مائية. |

## انظر أيضًا

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetWatermarkToImages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


يضيف علامة مائية صورة إلى المستند مع خيارات. يُولِّد المخرجات كصور.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Watermarker::SetWatermarkToImages(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions, const System::SharedPtr<System::IO::Stream> &watermarkImageStream, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | دفق الإدخال. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | خيارات الحفظ. |
| watermarkImageStream | const System::SharedPtr\<System::IO::Stream\>\& | تدفق الصورة المعروض كعلامة مائية. |
| خيارات | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | يحدد خيارات إضافية للعلامة المائية الصورة. |

## انظر أيضًا

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetWatermarkToImages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&) method


يضيف علامة مائية نصية إلى المستند مع خيارات. يُولِّد المخرجات كصور.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Watermarker::SetWatermarkToImages(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions, const System::String &watermarkText)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | تدفق ملف الإدخال. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | خيارات الحفظ. |
| watermarkText | const System::String\& | النص المعروض كعلامة مائية. |

## انظر أيضًا

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetWatermarkToImages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) method


يضيف علامة مائية نصية إلى المستند مع خيارات. يُولِّد المخرجات كصور.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Watermarker::SetWatermarkToImages(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions, const System::String &watermarkText, const System::SharedPtr<Aspose::Words::TextWatermarkOptions> &options)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | تدفق ملف الإدخال. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | خيارات الحفظ. |
| watermarkText | const System::String\& | النص المعروض كعلامة مائية. |
| خيارات | const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\& | يحدد خيارات إضافية للعلامة المائية النصية. |

## انظر أيضًا

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetWatermarkToImages(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::ArrayPtr\<uint8_t\>\&) method


يضيف علامة مائية صورة إلى المستند مع خيارات. يُولِّد المخرجات كصور.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Watermarker::SetWatermarkToImages(const System::String &inputFileName, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions, const System::ArrayPtr<uint8_t> &watermarkImageBytes)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| inputFileName | const System::String\& | اسم ملف الإدخال. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | خيارات الحفظ. |
| watermarkImageBytes | const System::ArrayPtr\<uint8_t\>\& | بايتات الصورة التي تُعرض كعلامة مائية. |

## انظر أيضًا

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetWatermarkToImages(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::ArrayPtr\<uint8_t\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


يضيف علامة مائية صورة إلى المستند مع خيارات. يُولِّد المخرجات كصور.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Watermarker::SetWatermarkToImages(const System::String &inputFileName, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions, const System::ArrayPtr<uint8_t> &watermarkImageBytes, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| inputFileName | const System::String\& | اسم ملف الإدخال. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | خيارات الحفظ. |
| watermarkImageBytes | const System::ArrayPtr\<uint8_t\>\& | بايتات الصورة التي تُعرض كعلامة مائية. |
| خيارات | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | يحدد خيارات إضافية للعلامة المائية الصورة. |

## انظر أيضًا

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetWatermarkToImages(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&) method


يضيف علامة مائية نصية إلى المستند مع خيارات. يُولِّد المخرجات كصور.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Watermarker::SetWatermarkToImages(const System::String &inputFileName, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions, const System::String &watermarkText)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| inputFileName | const System::String\& | اسم ملف الإدخال. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | خيارات الحفظ. |
| watermarkText | const System::String\& | النص المعروض كعلامة مائية. |

## انظر أيضًا

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetWatermarkToImages(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) method


يضيف علامة مائية نصية إلى المستند مع خيارات. يُولِّد المخرجات كصور.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Watermarker::SetWatermarkToImages(const System::String &inputFileName, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions, const System::String &watermarkText, const System::SharedPtr<Aspose::Words::TextWatermarkOptions> &options)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| inputFileName | const System::String\& | اسم ملف الإدخال. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | خيارات الحفظ. |
| watermarkText | const System::String\& | النص المعروض كعلامة مائية. |
| خيارات | const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\& | يحدد خيارات إضافية للعلامة المائية النصية. |

## انظر أيضًا

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
