---
title: "Aspose::Words::LowCode::Splitter::Split طريقة"
linktitle: "قسّم"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::LowCode::Splitter::Split طريقة. يقسم مستندًا من تدفق إدخال إلى أجزاء متعددة بناءً على خيارات القسمة المحددة ويعيد الأجزاء الناتجة كمصفوفة من التدفقات بالتنسيق المحدد للحفظ في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.lowcode/splitter/split/
---
## Splitter::Split(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) method


يقسم مستندًا من تدفق إدخال إلى أجزاء متعددة بناءً على خيارات التقسيم المحددة ويعيد الأجزاء الناتجة كمصفوفة من التدفقات بالتنسيق المحدد للحفظ.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Splitter::Split(const System::SharedPtr<System::IO::Stream> &inputStream, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<Aspose::Words::LowCode::SplitOptions> &options)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | دفق الإدخال. |
| saveFormat | Aspose::Words::SaveFormat | تنسيق الحفظ. |
| options | const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\& | [Document](../../../aspose.words/document/) خيارات القسمة. |

## انظر أيضًا

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [SplitOptions](../../splitoptions/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::Split(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) method


يقسم مستندًا من تدفق إدخال إلى أجزاء متعددة بناءً على خيارات التقسيم المحددة ويعيد الأجزاء الناتجة كمصفوفة من التدفقات بالتنسيق المحدد للحفظ.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Splitter::Split(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<Aspose::Words::LowCode::SplitOptions> &options)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | دفق الإدخال. |
| saveOptions | const System::SharedPtr\\<Aspose::Words::Saving::SaveOptions\\>\\& | خيارات الحفظ. |
| options | const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\& | [Document](../../../aspose.words/document/) خيارات القسمة. |

## انظر أيضًا

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [SplitOptions](../../splitoptions/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::Split(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) method


يقسم المستند إلى أجزاء متعددة بناءً على خيارات التقسيم المحددة ويحفظ الأجزاء الناتجة إلى ملفات بالتنسيق المحدد للحفظ.

```cpp
static void Aspose::Words::LowCode::Splitter::Split(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<Aspose::Words::LowCode::SplitOptions> &options)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| inputFileName | const System::String\& | اسم ملف الإدخال. |
| outputFileName | const System::String\& | اسم ملف الإخراج المستخدم لإنشاء اسم ملف لأجزاء المستند باستخدام القاعدة "outputFile_partIndex.extension" |
| saveFormat | Aspose::Words::SaveFormat | تنسيق الحفظ. |
| options | const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\& | [Document](../../../aspose.words/document/) خيارات القسمة. |

## انظر أيضًا

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [SplitOptions](../../splitoptions/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::Split(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) method


يقسم المستند إلى أجزاء متعددة بناءً على خيارات التقسيم المحددة ويحفظ الأجزاء الناتجة إلى ملفات. يتم تحديد تنسيق ملف الإخراج بناءً على امتداد اسم ملف الإخراج.

```cpp
static void Aspose::Words::LowCode::Splitter::Split(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::LowCode::SplitOptions> &options)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| inputFileName | const System::String\& | اسم ملف الإدخال. |
| outputFileName | const System::String\& | اسم ملف الإخراج المستخدم لإنشاء اسم ملف لأجزاء المستند باستخدام القاعدة "outputFile_partIndex.extension" |
| options | const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\& | [Document](../../../aspose.words/document/) خيارات القسمة. |

## انظر أيضًا

* Class [SplitOptions](../../splitoptions/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::Split(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) method


يقسم المستند إلى أجزاء متعددة بناءً على خيارات التقسيم المحددة ويحفظ الأجزاء الناتجة إلى ملفات بالتنسيق المحدد للحفظ.

```cpp
static void Aspose::Words::LowCode::Splitter::Split(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<Aspose::Words::LowCode::SplitOptions> &options)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| inputFileName | const System::String\& | اسم ملف الإدخال. |
| outputFileName | const System::String\& | اسم ملف الإخراج المستخدم لإنشاء اسم ملف لأجزاء المستند باستخدام القاعدة "outputFile_partIndex.extension" |
| saveOptions | const System::SharedPtr\\<Aspose::Words::Saving::SaveOptions\\>\\& | خيارات الحفظ. |
| options | const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\& | [Document](../../../aspose.words/document/) خيارات القسمة. |

## انظر أيضًا

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [SplitOptions](../../splitoptions/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
