---
title: "Aspose::Words::LowCode::Replacer::ReplaceToImages طريقة"
linktitle: "ReplaceToImages"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::LowCode::Replacer::ReplaceToImages طريقة. يستبدل جميع تكرارات نمط تعبير عادي محدد بسلسلة استبدال في ملف الإدخال. يُظهر الناتج كصور في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.lowcode/replacer/replacetoimages/
---
## Replacer::ReplaceToImages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) method


يستبدل جميع تكرارات نمط تعبير نمطي محدد بسلسلة استبدال في ملف الإدخال. يُولّد المخرجات كصور.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Replacer::ReplaceToImages(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | تدفق ملف الإدخال. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | خيارات الحفظ. |
| نمط | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | نمط تعبير عادي يُستخدم للعثور على التطابقات. |
| استبدال | const System::String\& | سلسلة لاستبدال جميع حدوث النمط. |

## انظر أيضًا

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::ReplaceToImages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


يستبدل جميع تكرارات نمط تعبير نمطي محدد بسلسلة استبدال في ملف الإدخال. يُولّد المخرجات كصور.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Replacer::ReplaceToImages(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | تدفق ملف الإدخال. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | خيارات الحفظ. |
| نمط | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | نمط تعبير عادي يُستخدم للعثور على التطابقات. |
| استبدال | const System::String\& | سلسلة لاستبدال جميع حدوث النمط. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | كائن [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) لتحديد خيارات إضافية. |

## انظر أيضًا

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::ReplaceToImages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, const System::String\&) method


يستبدل جميع تكرارات نمط سلسلة أحرف محدد بسلسلة استبدال في ملف الإدخال. يُولّد المخرجات كصور.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Replacer::ReplaceToImages(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions, const System::String &pattern, const System::String &replacement)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | تدفق ملف الإدخال. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | خيارات الحفظ. |
| نمط | const System::String\& | سلسلة لاستبدالها. |
| استبدال | const System::String\& | سلسلة لاستبدال جميع حدوث النمط. |

## انظر أيضًا

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::ReplaceToImages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


يستبدل جميع تكرارات نمط سلسلة أحرف محدد بسلسلة استبدال في ملف الإدخال. يُولّد المخرجات كصور.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Replacer::ReplaceToImages(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions, const System::String &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | تدفق ملف الإدخال. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | خيارات الحفظ. |
| نمط | const System::String\& | سلسلة لاستبدالها. |
| استبدال | const System::String\& | سلسلة لاستبدال جميع حدوث النمط. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | كائن [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) لتحديد خيارات إضافية. |

## انظر أيضًا

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::ReplaceToImages(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) method


يستبدل جميع تكرارات نمط تعبير نمطي محدد بسلسلة استبدال في ملف الإدخال. يُولّد المخرجات كصور.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Replacer::ReplaceToImages(const System::String &inputFileName, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| inputFileName | const System::String\& | اسم ملف الإدخال. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | خيارات الحفظ. |
| نمط | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | نمط تعبير عادي يُستخدم للعثور على التطابقات. |
| استبدال | const System::String\& | سلسلة لاستبدال جميع حدوث النمط. |

## انظر أيضًا

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::ReplaceToImages(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


يستبدل جميع تكرارات نمط تعبير نمطي محدد بسلسلة استبدال في ملف الإدخال. يُولّد المخرجات كصور.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Replacer::ReplaceToImages(const System::String &inputFileName, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| inputFileName | const System::String\& | اسم ملف الإدخال. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | خيارات الحفظ. |
| نمط | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | نمط تعبير عادي يُستخدم للعثور على التطابقات. |
| استبدال | const System::String\& | سلسلة لاستبدال جميع حدوث النمط. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | كائن [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) لتحديد خيارات إضافية. |

## انظر أيضًا

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::ReplaceToImages(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, const System::String\&) method


يستبدل جميع تكرارات نمط سلسلة أحرف محدد بسلسلة استبدال في ملف الإدخال. يُولّد المخرجات كصور.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Replacer::ReplaceToImages(const System::String &inputFileName, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions, const System::String &pattern, const System::String &replacement)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| inputFileName | const System::String\& | اسم ملف الإدخال. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | خيارات الحفظ. |
| نمط | const System::String\& | سلسلة لاستبدالها. |
| استبدال | const System::String\& | سلسلة لاستبدال جميع حدوث النمط. |

## انظر أيضًا

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::ReplaceToImages(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


يستبدل جميع تكرارات نمط سلسلة أحرف محدد بسلسلة استبدال في ملف الإدخال. يُولّد المخرجات كصور.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Replacer::ReplaceToImages(const System::String &inputFileName, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions, const System::String &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| inputFileName | const System::String\& | اسم ملف الإدخال. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | خيارات الحفظ. |
| نمط | const System::String\& | سلسلة لاستبدالها. |
| استبدال | const System::String\& | سلسلة لاستبدال جميع حدوث النمط. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | كائن [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) لتحديد خيارات إضافية. |

## انظر أيضًا

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
