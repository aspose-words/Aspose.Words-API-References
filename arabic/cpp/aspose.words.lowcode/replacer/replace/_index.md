---
title: "Aspose::Words::LowCode::Replacer::Replace طريقة"
linktitle: "Replace"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::LowCode::Replacer::Replace طريقة. يستبدل جميع تكرارات نمط سلسلة أحرف محدد بسلسلة استبدال في تدفق الإدخال باستخدام تعبير عادي، مع تنسيق الحفظ المحدد وخيارات إضافية في C++."
type: docs
weight: 1000
url: /ar/cpp/aspose.words.lowcode/replacer/replace/
---
## Replacer::Replace(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) method


يستبدل جميع تكرارات نمط سلسلة أحرف محدد بسلسلة استبدال في تدفق الإدخال باستخدام تعبير نمطي، مع تنسيق الحفظ المحدد وخيارات إضافية.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | دفق الإدخال. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | تدفق الإخراج. |
| saveFormat | Aspose::Words::SaveFormat | تنسيق الحفظ. |
| نمط | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | نمط تعبير عادي يُستخدم للعثور على التطابقات. |
| استبدال | const System::String\& | سلسلة لاستبدال جميع حدوث النمط. |

### ReturnValue

عدد عمليات الاستبدال التي تم إجراؤها.
## ملاحظات


إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، سيتم حفظ الصفحة الأولى فقط من الإخراج إلى الدفق المحدد.

إذا كان تنسيق الإخراج TIFF، سيتم حفظ الإخراج كملف TIFF متعدد الإطارات واحد إلى الدفق المحدد.

## انظر أيضًا

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


يستبدل جميع تكرارات نمط سلسلة أحرف محدد بسلسلة استبدال في تدفق الإدخال باستخدام تعبير نمطي، مع تنسيق الحفظ المحدد وخيارات إضافية.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | دفق الإدخال. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | تدفق الإخراج. |
| saveFormat | Aspose::Words::SaveFormat | تنسيق الحفظ. |
| نمط | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | نمط تعبير عادي يُستخدم للعثور على التطابقات. |
| استبدال | const System::String\& | سلسلة لاستبدال جميع حدوث النمط. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | كائن [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) لتحديد خيارات إضافية. |

### ReturnValue

عدد عمليات الاستبدال التي تم إجراؤها.
## ملاحظات


إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، سيتم حفظ الصفحة الأولى فقط من الإخراج إلى الدفق المحدد.

إذا كان تنسيق الإخراج TIFF، سيتم حفظ الإخراج كملف TIFF متعدد الإطارات واحد إلى الدفق المحدد.

## انظر أيضًا

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, const System::String\&) method


يستبدل جميع تكرارات نمط سلسلة الأحرف المحدد بسلسلة استبدال في تدفق الإدخال، مع تنسيق الحفظ المحدد وخيارات إضافية.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::String &pattern, const System::String &replacement)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | دفق الإدخال. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | تدفق الإخراج. |
| saveFormat | Aspose::Words::SaveFormat | تنسيق الحفظ. |
| نمط | const System::String\& | سلسلة لاستبدالها. |
| استبدال | const System::String\& | سلسلة لاستبدال جميع حدوث النمط. |

### ReturnValue

عدد عمليات الاستبدال التي تم إجراؤها.
## ملاحظات


إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، سيتم حفظ الصفحة الأولى فقط من الإخراج إلى الدفق المحدد.

إذا كان تنسيق الإخراج TIFF، سيتم حفظ الإخراج كملف TIFF متعدد الإطارات واحد إلى الدفق المحدد.

## انظر أيضًا

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


يستبدل جميع تكرارات نمط سلسلة الأحرف المحدد بسلسلة استبدال في تدفق الإدخال، مع تنسيق الحفظ المحدد وخيارات إضافية.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::String &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | دفق الإدخال. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | تدفق الإخراج. |
| saveFormat | Aspose::Words::SaveFormat | تنسيق الحفظ. |
| نمط | const System::String\& | سلسلة لاستبدالها. |
| استبدال | const System::String\& | سلسلة لاستبدال جميع حدوث النمط. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | كائن [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) لتحديد خيارات إضافية. |

### ReturnValue

عدد عمليات الاستبدال التي تم إجراؤها.
## ملاحظات


إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، سيتم حفظ الصفحة الأولى فقط من الإخراج إلى الدفق المحدد.

إذا كان تنسيق الإخراج TIFF، سيتم حفظ الإخراج كملف TIFF متعدد الإطارات واحد إلى الدفق المحدد.

## انظر أيضًا

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) method


يستبدل جميع تكرارات نمط سلسلة أحرف محدد بسلسلة استبدال في تدفق الإدخال باستخدام تعبير نمطي، مع تنسيق الحفظ المحدد وخيارات إضافية.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | دفق الإدخال. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | تدفق الإخراج. |
| saveOptions | const System::SharedPtr\\<Aspose::Words::Saving::SaveOptions\\>\\& | خيارات الحفظ. |
| نمط | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | نمط تعبير عادي يُستخدم للعثور على التطابقات. |
| استبدال | const System::String\& | سلسلة لاستبدال جميع حدوث النمط. |

### ReturnValue

عدد عمليات الاستبدال التي تم إجراؤها.
## ملاحظات


إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، سيتم حفظ الصفحة الأولى فقط من الإخراج إلى الدفق المحدد.

إذا كان تنسيق الإخراج TIFF، سيتم حفظ الإخراج كملف TIFF متعدد الإطارات واحد إلى الدفق المحدد.

## انظر أيضًا

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


يستبدل جميع تكرارات نمط سلسلة أحرف محدد بسلسلة استبدال في تدفق الإدخال باستخدام تعبير نمطي، مع تنسيق الحفظ المحدد وخيارات إضافية.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | دفق الإدخال. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | تدفق الإخراج. |
| saveOptions | const System::SharedPtr\\<Aspose::Words::Saving::SaveOptions\\>\\& | خيارات الحفظ. |
| نمط | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | نمط تعبير عادي يُستخدم للعثور على التطابقات. |
| استبدال | const System::String\& | سلسلة لاستبدال جميع حدوث النمط. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | كائن [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) لتحديد خيارات إضافية. |

### ReturnValue

عدد عمليات الاستبدال التي تم إجراؤها.
## ملاحظات


إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، سيتم حفظ الصفحة الأولى فقط من الإخراج إلى الدفق المحدد.

إذا كان تنسيق الإخراج TIFF، سيتم حفظ الإخراج كملف TIFF متعدد الإطارات واحد إلى الدفق المحدد.

## انظر أيضًا

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::String\&) method


يستبدل جميع تكرارات نمط سلسلة الأحرف المحدد بسلسلة استبدال في تدفق الإدخال، مع تنسيق الحفظ المحدد وخيارات إضافية.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &pattern, const System::String &replacement)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | دفق الإدخال. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | تدفق الإخراج. |
| saveOptions | const System::SharedPtr\\<Aspose::Words::Saving::SaveOptions\\>\\& | خيارات الحفظ. |
| نمط | const System::String\& | سلسلة لاستبدالها. |
| استبدال | const System::String\& | سلسلة لاستبدال جميع حدوث النمط. |

### ReturnValue

عدد عمليات الاستبدال التي تم إجراؤها.
## ملاحظات


إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، سيتم حفظ الصفحة الأولى فقط من الإخراج إلى الدفق المحدد.

إذا كان تنسيق الإخراج TIFF، سيتم حفظ الإخراج كملف TIFF متعدد الإطارات واحد إلى الدفق المحدد.

## انظر أيضًا

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


يستبدل جميع تكرارات نمط سلسلة الأحرف المحدد بسلسلة استبدال في تدفق الإدخال، مع تنسيق الحفظ المحدد وخيارات إضافية.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | دفق الإدخال. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | تدفق الإخراج. |
| saveOptions | const System::SharedPtr\\<Aspose::Words::Saving::SaveOptions\\>\\& | خيارات الحفظ. |
| نمط | const System::String\& | سلسلة لاستبدالها. |
| استبدال | const System::String\& | سلسلة لاستبدال جميع حدوث النمط. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | كائن [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) لتحديد خيارات إضافية. |

### ReturnValue

عدد عمليات الاستبدال التي تم إجراؤها.
## ملاحظات


إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، سيتم حفظ الصفحة الأولى فقط من الإخراج إلى الدفق المحدد.

إذا كان تنسيق الإخراج TIFF، سيتم حفظ الإخراج كملف TIFF متعدد الإطارات واحد إلى الدفق المحدد.

## انظر أيضًا

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) method


يستبدل جميع تكرارات نمط سلسلة أحرف محدد بسلسلة استبدال في ملف الإدخال باستخدام تعبير نمطي، مع تنسيق الحفظ المحدد وخيارات إضافية.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| inputFileName | const System::String\& | اسم ملف الإدخال. |
| outputFileName | const System::String\& | اسم ملف الإخراج. |
| saveFormat | Aspose::Words::SaveFormat | تنسيق الحفظ. |
| نمط | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | نمط تعبير عادي يُستخدم للعثور على التطابقات. |
| استبدال | const System::String\& | سلسلة لاستبدال جميع حدوث النمط. |

### ReturnValue

عدد عمليات الاستبدال التي تم إجراؤها.
## ملاحظات


إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، سيتم حفظ كل صفحة من الإخراج كملف منفصل. سيُستخدم اسم ملف الإخراج المحدد لتوليد أسماء الملفات لكل جزء وفق القاعدة: outputFile_partIndex.extension.

إذا كان تنسيق الإخراج TIFF، سيتم حفظ الإخراج كملف TIFF متعدد الإطارات واحد.

## انظر أيضًا

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


يستبدل جميع تكرارات نمط سلسلة أحرف محدد بسلسلة استبدال في ملف الإدخال باستخدام تعبير نمطي، مع تنسيق الحفظ المحدد وخيارات إضافية.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| inputFileName | const System::String\& | اسم ملف الإدخال. |
| outputFileName | const System::String\& | اسم ملف الإخراج. |
| saveFormat | Aspose::Words::SaveFormat | تنسيق الحفظ. |
| نمط | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | نمط تعبير عادي يُستخدم للعثور على التطابقات. |
| استبدال | const System::String\& | سلسلة لاستبدال جميع حدوث النمط. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | كائن [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) لتحديد خيارات إضافية. |

### ReturnValue

عدد عمليات الاستبدال التي تم إجراؤها.
## ملاحظات


إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، سيتم حفظ كل صفحة من الإخراج كملف منفصل. سيُستخدم اسم ملف الإخراج المحدد لتوليد أسماء الملفات لكل جزء وفق القاعدة: outputFile_partIndex.extension.

إذا كان تنسيق الإخراج TIFF، سيتم حفظ الإخراج كملف TIFF متعدد الإطارات واحد.

## انظر أيضًا

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, const System::String\&) method


يستبدل جميع تكرارات نمط سلسلة الأحرف المحدد بسلسلة استبدال في ملف الإدخال، مع تنسيق الحفظ المحدد وخيارات إضافية.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::String &pattern, const System::String &replacement)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| inputFileName | const System::String\& | اسم ملف الإدخال. |
| outputFileName | const System::String\& | اسم ملف الإخراج. |
| saveFormat | Aspose::Words::SaveFormat | تنسيق الحفظ. |
| نمط | const System::String\& | سلسلة لاستبدالها. |
| استبدال | const System::String\& | سلسلة لاستبدال جميع حدوث النمط. |

### ReturnValue

عدد عمليات الاستبدال التي تم إجراؤها.
## ملاحظات


إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، سيتم حفظ كل صفحة من الإخراج كملف منفصل. سيُستخدم اسم ملف الإخراج المحدد لتوليد أسماء الملفات لكل جزء وفق القاعدة: outputFile_partIndex.extension.

إذا كان تنسيق الإخراج TIFF، سيتم حفظ الإخراج كملف TIFF متعدد الإطارات واحد.

## انظر أيضًا

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


يستبدل جميع تكرارات نمط سلسلة الأحرف المحدد بسلسلة استبدال في ملف الإدخال، مع تنسيق الحفظ المحدد وخيارات إضافية.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::String &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| inputFileName | const System::String\& | اسم ملف الإدخال. |
| outputFileName | const System::String\& | اسم ملف الإخراج. |
| saveFormat | Aspose::Words::SaveFormat | تنسيق الحفظ. |
| نمط | const System::String\& | سلسلة لاستبدالها. |
| استبدال | const System::String\& | سلسلة لاستبدال جميع حدوث النمط. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | كائن [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) لتحديد خيارات إضافية. |

### ReturnValue

عدد عمليات الاستبدال التي تم إجراؤها.
## ملاحظات


إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، سيتم حفظ كل صفحة من الإخراج كملف منفصل. سيُستخدم اسم ملف الإخراج المحدد لتوليد أسماء الملفات لكل جزء وفق القاعدة: outputFile_partIndex.extension.

إذا كان تنسيق الإخراج TIFF، سيتم حفظ الإخراج كملف TIFF متعدد الإطارات واحد.

## انظر أيضًا

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) method


يستبدل جميع تكرارات نمط سلسلة أحرف محدد بسلسلة استبدال في ملف الإدخال باستخدام تعبير نمطي، مع تنسيق الحفظ المحدد وخيارات إضافية.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| inputFileName | const System::String\& | اسم ملف الإدخال. |
| outputFileName | const System::String\& | اسم ملف الإخراج. |
| saveOptions | const System::SharedPtr\\<Aspose::Words::Saving::SaveOptions\\>\\& | خيارات الحفظ. |
| نمط | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | نمط تعبير عادي يُستخدم للعثور على التطابقات. |
| استبدال | const System::String\& | سلسلة لاستبدال جميع حدوث النمط. |

### ReturnValue

عدد عمليات الاستبدال التي تم إجراؤها.
## ملاحظات


إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، سيتم حفظ كل صفحة من الإخراج كملف منفصل. سيُستخدم اسم ملف الإخراج المحدد لتوليد أسماء الملفات لكل جزء وفق القاعدة: outputFile_partIndex.extension.

إذا كان تنسيق الإخراج TIFF، سيتم حفظ الإخراج كملف TIFF متعدد الإطارات واحد.

## انظر أيضًا

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


يستبدل جميع تكرارات نمط سلسلة أحرف محدد بسلسلة استبدال في ملف الإدخال باستخدام تعبير نمطي، مع تنسيق الحفظ المحدد وخيارات إضافية.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| inputFileName | const System::String\& | اسم ملف الإدخال. |
| outputFileName | const System::String\& | اسم ملف الإخراج. |
| saveOptions | const System::SharedPtr\\<Aspose::Words::Saving::SaveOptions\\>\\& | خيارات الحفظ. |
| نمط | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | نمط تعبير عادي يُستخدم للعثور على التطابقات. |
| استبدال | const System::String\& | سلسلة لاستبدال جميع حدوث النمط. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | كائن [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) لتحديد خيارات إضافية. |

### ReturnValue

عدد عمليات الاستبدال التي تم إجراؤها.
## ملاحظات


إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، سيتم حفظ كل صفحة من الإخراج كملف منفصل. سيُستخدم اسم ملف الإخراج المحدد لتوليد أسماء الملفات لكل جزء وفق القاعدة: outputFile_partIndex.extension.

إذا كان تنسيق الإخراج TIFF، سيتم حفظ الإخراج كملف TIFF متعدد الإطارات واحد.

## انظر أيضًا

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::String\&) method


يستبدل جميع تكرارات نمط سلسلة الأحرف المحدد بسلسلة استبدال في ملف الإدخال، مع تنسيق الحفظ المحدد وخيارات إضافية.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &pattern, const System::String &replacement)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| inputFileName | const System::String\& | اسم ملف الإدخال. |
| outputFileName | const System::String\& | اسم ملف الإخراج. |
| saveOptions | const System::SharedPtr\\<Aspose::Words::Saving::SaveOptions\\>\\& | خيارات الحفظ. |
| نمط | const System::String\& | سلسلة لاستبدالها. |
| استبدال | const System::String\& | سلسلة لاستبدال جميع حدوث النمط. |

### ReturnValue

عدد عمليات الاستبدال التي تم إجراؤها.
## ملاحظات


إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، سيتم حفظ كل صفحة من الإخراج كملف منفصل. سيُستخدم اسم ملف الإخراج المحدد لتوليد أسماء الملفات لكل جزء وفق القاعدة: outputFile_partIndex.extension.

إذا كان تنسيق الإخراج TIFF، سيتم حفظ الإخراج كملف TIFF متعدد الإطارات واحد.

## انظر أيضًا

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


يستبدل جميع تكرارات نمط سلسلة الأحرف المحدد بسلسلة استبدال في ملف الإدخال، مع تنسيق الحفظ المحدد وخيارات إضافية.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| inputFileName | const System::String\& | اسم ملف الإدخال. |
| outputFileName | const System::String\& | اسم ملف الإخراج. |
| saveOptions | const System::SharedPtr\\<Aspose::Words::Saving::SaveOptions\\>\\& | خيارات الحفظ. |
| نمط | const System::String\& | سلسلة لاستبدالها. |
| استبدال | const System::String\& | سلسلة لاستبدال جميع حدوث النمط. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | كائن [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) لتحديد خيارات إضافية. |

### ReturnValue

عدد عمليات الاستبدال التي تم إجراؤها.
## ملاحظات


إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، سيتم حفظ كل صفحة من الإخراج كملف منفصل. سيُستخدم اسم ملف الإخراج المحدد لتوليد أسماء الملفات لكل جزء وفق القاعدة: outputFile_partIndex.extension.

إذا كان تنسيق الإخراج TIFF، سيتم حفظ الإخراج كملف TIFF متعدد الإطارات واحد.

## انظر أيضًا

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) method


يستبدل جميع تكرارات نمط سلسلة الأحرف المحدد بسلسلة استبدال في ملف الإدخال باستخدام تعبير عادي.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| inputFileName | const System::String\& | اسم ملف الإدخال. |
| outputFileName | const System::String\& | اسم ملف الإخراج. |
| نمط | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | نمط تعبير عادي يُستخدم للعثور على التطابقات. |
| استبدال | const System::String\& | سلسلة لاستبدال جميع حدوث النمط. |

### ReturnValue

عدد عمليات الاستبدال التي تم إجراؤها.
## ملاحظات


إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، سيتم حفظ كل صفحة من الإخراج كملف منفصل. سيُستخدم اسم ملف الإخراج المحدد لتوليد أسماء الملفات لكل جزء وفق القاعدة: outputFile_partIndex.extension.

إذا كان تنسيق الإخراج TIFF، سيتم حفظ الإخراج كملف TIFF متعدد الإطارات واحد.

## انظر أيضًا

* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, const System::String\&, const System::String\&) method


يستبدل جميع تكرارات نمط سلسلة الأحرف المحدد بسلسلة استبدال في ملف الإدخال.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, const System::String &pattern, const System::String &replacement)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| inputFileName | const System::String\& | اسم ملف الإدخال. |
| outputFileName | const System::String\& | اسم ملف الإخراج. |
| نمط | const System::String\& | سلسلة لاستبدالها. |
| استبدال | const System::String\& | سلسلة لاستبدال جميع حدوث النمط. |

### ReturnValue

عدد عمليات الاستبدال التي تم إجراؤها.
## ملاحظات


إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، سيتم حفظ كل صفحة من الإخراج كملف منفصل. سيُستخدم اسم ملف الإخراج المحدد لتوليد أسماء الملفات لكل جزء وفق القاعدة: outputFile_partIndex.extension.

إذا كان تنسيق الإخراج TIFF، سيتم حفظ الإخراج كملف TIFF متعدد الإطارات واحد.

## انظر أيضًا

* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
