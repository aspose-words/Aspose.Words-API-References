---
title: Replacer.Replace
linktitle: Replace
articleTitle: Replace
second_title: Aspose.Words لـ .NET
description: استبدل بسهولة جميع حالات سلسلة نصية محددة في ملف الإدخال باستخدام طريقة الاستبدال. حسّن تحرير نصوصك اليوم!
type: docs
weight: 20
url: /ar/net/aspose.words.lowcode/replacer/replace/
---
## Replace(*string, string, string, string*) {#replace_8}

يستبدل جميع حالات نمط سلسلة أحرف محددة بسلسلة بديلة في ملف الإدخال.

```csharp
public static int Replace(string inputFileName, string outputFileName, string pattern, 
    string replacement)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| inputFileName | String | اسم ملف الإدخال. |
| outputFileName | String | اسم ملف الإخراج. |
| pattern | String | سلسلة ليتم استبدالها. |
| replacement | String | سلسلة لاستبدال كافة حالات النمط. |

### قيمة الإرجاع

عدد الاستبدالات التي تم إجراؤها.

## ملاحظات

إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، فسيتم حفظ كل صفحة من الإخراج كملف منفصل. سيتم استخدام اسم ملف الإخراج المحدد لإنشاء أسماء ملفات لكل جزء وفقًا للقاعدة: outputFile_partIndex.extension.

إذا كان تنسيق الإخراج هو TIFF، فسيتم حفظ الإخراج كملف TIFF متعدد الإطارات.

## أمثلة

يوضح كيفية استبدال السلسلة في المستند.

```csharp
// هناك عدة طرق لاستبدال السلسلة في المستند:
string doc = MyDir + "Footer.docx";
string pattern = "(C)2006 Aspose Pty Ltd.";
string replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

FindReplaceOptions options = new FindReplaceOptions();
options.FindWholeWordsOnly = false;
Replacer.Replace(doc, ArtifactsDir + "LowCode.Replace.1.docx", pattern, replacement);
Replacer.Replace(doc, ArtifactsDir + "LowCode.Replace.2.docx", SaveFormat.Docx, pattern, replacement);
Replacer.Replace(doc, ArtifactsDir + "LowCode.Replace.3.docx", SaveFormat.Docx, pattern, replacement, options);
```

### أنظر أيضا

* class [Replacer](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)

---

## Replace(*string, string, [SaveFormat](../../../aspose.words/saveformat/), string, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replace_4}

يستبدل جميع حالات نمط سلسلة أحرف محددة بسلسلة بديلة في ملف الإدخال، مع تنسيق الحفظ المحدد والخيارات الإضافية.

```csharp
public static int Replace(string inputFileName, string outputFileName, SaveFormat saveFormat, 
    string pattern, string replacement, FindReplaceOptions options = null)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| inputFileName | String | اسم ملف الإدخال. |
| outputFileName | String | اسم ملف الإخراج. |
| saveFormat | SaveFormat | تنسيق الحفظ. |
| pattern | String | سلسلة ليتم استبدالها. |
| replacement | String | سلسلة لاستبدال كافة حالات النمط. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) كائن لتحديد خيارات إضافية. |

### قيمة الإرجاع

عدد الاستبدالات التي تم إجراؤها.

## ملاحظات

إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، فسيتم حفظ كل صفحة من الإخراج كملف منفصل. سيتم استخدام اسم ملف الإخراج المحدد لإنشاء أسماء ملفات لكل جزء وفقًا للقاعدة: outputFile_partIndex.extension.

إذا كان تنسيق الإخراج هو TIFF، فسيتم حفظ الإخراج كملف TIFF متعدد الإطارات.

## أمثلة

يوضح كيفية استبدال السلسلة في المستند.

```csharp
// هناك عدة طرق لاستبدال السلسلة في المستند:
string doc = MyDir + "Footer.docx";
string pattern = "(C)2006 Aspose Pty Ltd.";
string replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

FindReplaceOptions options = new FindReplaceOptions();
options.FindWholeWordsOnly = false;
Replacer.Replace(doc, ArtifactsDir + "LowCode.Replace.1.docx", pattern, replacement);
Replacer.Replace(doc, ArtifactsDir + "LowCode.Replace.2.docx", SaveFormat.Docx, pattern, replacement);
Replacer.Replace(doc, ArtifactsDir + "LowCode.Replace.3.docx", SaveFormat.Docx, pattern, replacement, options);
```

### أنظر أيضا

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Replacer](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)

---

## Replace(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), string, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replace_6}

يستبدل جميع حالات نمط سلسلة أحرف محددة بسلسلة بديلة في ملف الإدخال، مع تنسيق الحفظ المحدد والخيارات الإضافية.

```csharp
public static int Replace(string inputFileName, string outputFileName, SaveOptions saveOptions, 
    string pattern, string replacement, FindReplaceOptions options = null)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| inputFileName | String | اسم ملف الإدخال. |
| outputFileName | String | اسم ملف الإخراج. |
| saveOptions | SaveOptions | خيارات الحفظ. |
| pattern | String | سلسلة ليتم استبدالها. |
| replacement | String | سلسلة لاستبدال كافة حالات النمط. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) كائن لتحديد خيارات إضافية. |

### قيمة الإرجاع

عدد الاستبدالات التي تم إجراؤها.

## ملاحظات

إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، فسيتم حفظ كل صفحة من الإخراج كملف منفصل. سيتم استخدام اسم ملف الإخراج المحدد لإنشاء أسماء ملفات لكل جزء وفقًا للقاعدة: outputFile_partIndex.extension.

إذا كان تنسيق الإخراج هو TIFF، فسيتم حفظ الإخراج كملف TIFF متعدد الإطارات.

### أنظر أيضا

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Replacer](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)

---

## Replace(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), string, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replace}

يستبدل جميع حالات نمط سلسلة أحرف محددة بسلسلة بديلة في مجرى الإدخال، مع تنسيق الحفظ المحدد والخيارات الإضافية.

```csharp
public static int Replace(Stream inputStream, Stream outputStream, SaveFormat saveFormat, 
    string pattern, string replacement, FindReplaceOptions options = null)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| inputStream | Stream | مجرى الإدخال. |
| outputStream | Stream | تيار الإخراج. |
| saveFormat | SaveFormat | تنسيق الحفظ. |
| pattern | String | سلسلة ليتم استبدالها. |
| replacement | String | سلسلة لاستبدال كافة حالات النمط. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) كائن لتحديد خيارات إضافية. |

### قيمة الإرجاع

عدد الاستبدالات التي تم إجراؤها.

## ملاحظات

إذا كان تنسيق الإخراج عبارة عن صورة (BMP، أو EMF، أو EPS، أو GIF، أو JPEG، أو PNG، أو WebP)، فسيتم حفظ الصفحة الأولى فقط من الإخراج في التدفق المحدد.

إذا كان تنسيق الإخراج هو TIFF، فسيتم حفظ الإخراج كملف TIFF متعدد الإطارات إلى الدفق المحدد.

## أمثلة

يوضح كيفية استبدال السلسلة في المستند باستخدام المستندات من الدفق.

```csharp
// هناك عدة طرق لاستبدال السلسلة في المستند باستخدام المستندات من الدفق:
string pattern = "(C)2006 Aspose Pty Ltd.";
string replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

using (FileStream streamIn = new FileStream(MyDir + "Footer.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ReplaceStream.1.docx", FileMode.Create, FileAccess.ReadWrite))
        Replacer.Replace(streamIn, streamOut, SaveFormat.Docx, pattern, replacement);

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ReplaceStream.2.docx", FileMode.Create, FileAccess.ReadWrite))
    {
        FindReplaceOptions options = new FindReplaceOptions();
        options.FindWholeWordsOnly = false;
        Replacer.Replace(streamIn, streamOut, SaveFormat.Docx, pattern, replacement, options);
    }
}
```

### أنظر أيضا

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Replacer](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)

---

## Replace(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), string, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replace_2}

يستبدل جميع حالات نمط سلسلة أحرف محددة بسلسلة بديلة في مجرى الإدخال، مع تنسيق الحفظ المحدد والخيارات الإضافية.

```csharp
public static int Replace(Stream inputStream, Stream outputStream, SaveOptions saveOptions, 
    string pattern, string replacement, FindReplaceOptions options = null)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| inputStream | Stream | مجرى الإدخال. |
| outputStream | Stream | تيار الإخراج. |
| saveOptions | SaveOptions | خيارات الحفظ. |
| pattern | String | سلسلة ليتم استبدالها. |
| replacement | String | سلسلة لاستبدال كافة حالات النمط. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) كائن لتحديد خيارات إضافية. |

### قيمة الإرجاع

عدد الاستبدالات التي تم إجراؤها.

## ملاحظات

إذا كان تنسيق الإخراج عبارة عن صورة (BMP، أو EMF، أو EPS، أو GIF، أو JPEG، أو PNG، أو WebP)، فسيتم حفظ الصفحة الأولى فقط من الإخراج في التدفق المحدد.

إذا كان تنسيق الإخراج هو TIFF، فسيتم حفظ الإخراج كملف TIFF متعدد الإطارات إلى الدفق المحدد.

### أنظر أيضا

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Replacer](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)

---

## Replace(*string, string, Regex, string*) {#replace_9}

يستبدل جميع حالات نمط سلسلة أحرف محددة بسلسلة بديلة في ملف الإدخال باستخدام تعبير عادي.

```csharp
public static int Replace(string inputFileName, string outputFileName, Regex pattern, 
    string replacement)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| inputFileName | String | اسم ملف الإدخال. |
| outputFileName | String | اسم ملف الإخراج. |
| pattern | Regex | نمط تعبير منتظم يستخدم للعثور على المطابقات. |
| replacement | String | سلسلة لاستبدال كافة حالات النمط. |

### قيمة الإرجاع

عدد الاستبدالات التي تم إجراؤها.

## ملاحظات

إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، فسيتم حفظ كل صفحة من الإخراج كملف منفصل. سيتم استخدام اسم ملف الإخراج المحدد لإنشاء أسماء ملفات لكل جزء وفقًا للقاعدة: outputFile_partIndex.extension.

إذا كان تنسيق الإخراج هو TIFF، فسيتم حفظ الإخراج كملف TIFF متعدد الإطارات.

## أمثلة

يوضح كيفية استبدال السلسلة بـ regex في المستند.

```csharp
// هناك عدة طرق لاستبدال السلسلة بـ regex في المستند:
string doc = MyDir + "Footer.docx";
Regex pattern = new Regex("gr(a|e)y");
string replacement = "lavender";

Replacer.Replace(doc, ArtifactsDir + "LowCode.ReplaceRegex.1.docx", pattern, replacement);
Replacer.Replace(doc, ArtifactsDir + "LowCode.ReplaceRegex.2.docx", SaveFormat.Docx, pattern, replacement);
Replacer.Replace(doc, ArtifactsDir + "LowCode.ReplaceRegex.3.docx", SaveFormat.Docx, pattern, replacement, new FindReplaceOptions() { FindWholeWordsOnly = false });
```

### أنظر أيضا

* class [Replacer](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)

---

## Replace(*string, string, [SaveFormat](../../../aspose.words/saveformat/), Regex, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replace_5}

يستبدل جميع حالات نمط سلسلة أحرف محددة بسلسلة بديلة في ملف الإدخال باستخدام تعبير عادي، مع تنسيق الحفظ المحدد وخيارات إضافية.

```csharp
public static int Replace(string inputFileName, string outputFileName, SaveFormat saveFormat, 
    Regex pattern, string replacement, FindReplaceOptions options = null)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| inputFileName | String | اسم ملف الإدخال. |
| outputFileName | String | اسم ملف الإخراج. |
| saveFormat | SaveFormat | تنسيق الحفظ. |
| pattern | Regex | نمط تعبير منتظم يستخدم للعثور على المطابقات. |
| replacement | String | سلسلة لاستبدال كافة حالات النمط. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) كائن لتحديد خيارات إضافية. |

### قيمة الإرجاع

عدد الاستبدالات التي تم إجراؤها.

## ملاحظات

إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، فسيتم حفظ كل صفحة من الإخراج كملف منفصل. سيتم استخدام اسم ملف الإخراج المحدد لإنشاء أسماء ملفات لكل جزء وفقًا للقاعدة: outputFile_partIndex.extension.

إذا كان تنسيق الإخراج هو TIFF، فسيتم حفظ الإخراج كملف TIFF متعدد الإطارات.

## أمثلة

يوضح كيفية استبدال السلسلة بـ regex في المستند.

```csharp
// هناك عدة طرق لاستبدال السلسلة بـ regex في المستند:
string doc = MyDir + "Footer.docx";
Regex pattern = new Regex("gr(a|e)y");
string replacement = "lavender";

Replacer.Replace(doc, ArtifactsDir + "LowCode.ReplaceRegex.1.docx", pattern, replacement);
Replacer.Replace(doc, ArtifactsDir + "LowCode.ReplaceRegex.2.docx", SaveFormat.Docx, pattern, replacement);
Replacer.Replace(doc, ArtifactsDir + "LowCode.ReplaceRegex.3.docx", SaveFormat.Docx, pattern, replacement, new FindReplaceOptions() { FindWholeWordsOnly = false });
```

### أنظر أيضا

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Replacer](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)

---

## Replace(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), Regex, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replace_7}

يستبدل جميع حالات نمط سلسلة أحرف محددة بسلسلة بديلة في ملف الإدخال باستخدام تعبير عادي، مع تنسيق الحفظ المحدد وخيارات إضافية.

```csharp
public static int Replace(string inputFileName, string outputFileName, SaveOptions saveOptions, 
    Regex pattern, string replacement, FindReplaceOptions options = null)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| inputFileName | String | اسم ملف الإدخال. |
| outputFileName | String | اسم ملف الإخراج. |
| saveOptions | SaveOptions | خيارات الحفظ. |
| pattern | Regex | نمط تعبير منتظم يستخدم للعثور على المطابقات. |
| replacement | String | سلسلة لاستبدال كافة حالات النمط. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) كائن لتحديد خيارات إضافية. |

### قيمة الإرجاع

عدد الاستبدالات التي تم إجراؤها.

## ملاحظات

إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، فسيتم حفظ كل صفحة من الإخراج كملف منفصل. سيتم استخدام اسم ملف الإخراج المحدد لإنشاء أسماء ملفات لكل جزء وفقًا للقاعدة: outputFile_partIndex.extension.

إذا كان تنسيق الإخراج هو TIFF، فسيتم حفظ الإخراج كملف TIFF متعدد الإطارات.

### أنظر أيضا

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Replacer](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)

---

## Replace(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), Regex, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replace_1}

يستبدل جميع حالات نمط سلسلة أحرف محددة بسلسلة بديلة في مجرى الإدخال باستخدام تعبير عادي، مع تنسيق الحفظ المحدد وخيارات إضافية.

```csharp
public static int Replace(Stream inputStream, Stream outputStream, SaveFormat saveFormat, 
    Regex pattern, string replacement, FindReplaceOptions options = null)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| inputStream | Stream | مجرى الإدخال. |
| outputStream | Stream | تيار الإخراج. |
| saveFormat | SaveFormat | تنسيق الحفظ. |
| pattern | Regex | نمط تعبير منتظم يستخدم للعثور على المطابقات. |
| replacement | String | سلسلة لاستبدال كافة حالات النمط. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) كائن لتحديد خيارات إضافية. |

### قيمة الإرجاع

عدد الاستبدالات التي تم إجراؤها.

## ملاحظات

إذا كان تنسيق الإخراج عبارة عن صورة (BMP، أو EMF، أو EPS، أو GIF، أو JPEG، أو PNG، أو WebP)، فسيتم حفظ الصفحة الأولى فقط من الإخراج في التدفق المحدد.

إذا كان تنسيق الإخراج هو TIFF، فسيتم حفظ الإخراج كملف TIFF متعدد الإطارات إلى الدفق المحدد.

## أمثلة

يوضح كيفية استبدال السلسلة بـ regex في المستند باستخدام المستندات من التدفق.

```csharp
// هناك عدة طرق لاستبدال السلسلة بتعبير عادي في المستند باستخدام المستندات من التدفق:
Regex pattern = new Regex("gr(a|e)y");
string replacement = "lavender";

using (FileStream streamIn = new FileStream(MyDir + "Replace regex.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ReplaceStreamRegex.1.docx", FileMode.Create, FileAccess.ReadWrite))
        Replacer.Replace(streamIn, streamOut, SaveFormat.Docx, pattern, replacement);

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ReplaceStreamRegex.2.docx", FileMode.Create, FileAccess.ReadWrite))
        Replacer.Replace(streamIn, streamOut, SaveFormat.Docx, pattern, replacement, new FindReplaceOptions() { FindWholeWordsOnly = false });
}
```

### أنظر أيضا

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Replacer](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)

---

## Replace(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), Regex, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replace_3}

يستبدل جميع حالات نمط سلسلة أحرف محددة بسلسلة بديلة في مجرى الإدخال باستخدام تعبير عادي، مع تنسيق الحفظ المحدد وخيارات إضافية.

```csharp
public static int Replace(Stream inputStream, Stream outputStream, SaveOptions saveOptions, 
    Regex pattern, string replacement, FindReplaceOptions options = null)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| inputStream | Stream | مجرى الإدخال. |
| outputStream | Stream | تيار الإخراج. |
| saveOptions | SaveOptions | خيارات الحفظ. |
| pattern | Regex | نمط تعبير منتظم يستخدم للعثور على المطابقات. |
| replacement | String | سلسلة لاستبدال كافة حالات النمط. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) كائن لتحديد خيارات إضافية. |

### قيمة الإرجاع

عدد الاستبدالات التي تم إجراؤها.

## ملاحظات

إذا كان تنسيق الإخراج عبارة عن صورة (BMP، أو EMF، أو EPS، أو GIF، أو JPEG، أو PNG، أو WebP)، فسيتم حفظ الصفحة الأولى فقط من الإخراج في التدفق المحدد.

إذا كان تنسيق الإخراج هو TIFF، فسيتم حفظ الإخراج كملف TIFF متعدد الإطارات إلى الدفق المحدد.

### أنظر أيضا

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Replacer](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)
