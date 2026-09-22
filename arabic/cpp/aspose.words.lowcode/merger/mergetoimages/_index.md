---
title: "Aspose::Words::LowCode::Merger::MergeToImages طريقة"
linktitle: "MergeToImages"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::LowCode::Merger::MergeToImages طريقة. يقوم بدمج تدفقات مستندات الإدخال المعطاة في مستند خروج واحد باستخدام خيارات حفظ الصورة المحددة. يُظهر الناتج كصور في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.lowcode/merger/mergetoimages/
---
## Merger::MergeToImages(const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) method


يدمج تدفقات المستندات الإدخالية المعطاة في مستند إخراج واحد باستخدام خيارات حفظ الصور المحددة. يصوّر الإخراج إلى صور.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Merger::MergeToImages(const System::ArrayPtr<System::SharedPtr<System::IO::Stream>> &inputStreams, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions, Aspose::Words::LowCode::MergeFormatMode mergeFormatMode)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| inputStreams | const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\& | تدفقات ملفات الإدخال. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | خيارات الحفظ. |
| mergeFormatMode | Aspose::Words::LowCode::MergeFormatMode | يحدد كيفية دمج التنسيقات المتعارضة. |

## انظر أيضًا

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Enum [MergeFormatMode](../../mergeformatmode/)
* Class [Merger](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Merger::MergeToImages(const System::ArrayPtr\<System::String\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) method


يدمج المستندات الإدخالية المعطاة في مستند إخراج واحد باستخدام أسماء ملفات الإدخال والإخراج المحددة وخيارات الحفظ. يصوّر الإخراج إلى صور.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Merger::MergeToImages(const System::ArrayPtr<System::String> &inputFiles, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions, Aspose::Words::LowCode::MergeFormatMode mergeFormatMode)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| inputFiles | const System::ArrayPtr\<System::String\>\& | أسماء ملفات الإدخال. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | خيارات الحفظ. |
| mergeFormatMode | Aspose::Words::LowCode::MergeFormatMode | يحدد كيفية دمج التنسيقات المتعارضة. |

## انظر أيضًا

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Enum [MergeFormatMode](../../mergeformatmode/)
* Class [Merger](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
