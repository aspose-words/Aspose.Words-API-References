---
title: Splitter.ExtractPages
linktitle: ExtractPages
articleTitle: ExtractPages
second_title: Aspose.Words لـ .NET
description: استخرج صفحات محددة من أي مستند بسهولة باستخدام طريقة Splitter ExtractPages. احفظها بالتنسيق الذي تريده ليسهل الوصول إليها!
type: docs
weight: 20
url: /ar/net/aspose.words.lowcode/splitter/extractpages/
---
## ExtractPages(*string, string, int, int*) {#extractpages_4}

يستخرج نطاقًا محددًا من الصفحات من ملف مستند، ويحفظها في ملف جديد. يُحدَّد تنسيق ملف الإخراج بامتداد اسم الملف.

```csharp
public static void ExtractPages(string inputFileName, string outputFileName, int startPageIndex, 
    int pageCount)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| inputFileName | String | اسم ملف الإدخال. |
| outputFileName | String | اسم ملف الإخراج. |
| startPageIndex | Int32 | الفهرس المبني على الصفر للصفحة الأولى التي سيتم استخراجها. |
| pageCount | Int32 | عدد الصفحات المطلوب استخراجها. |

## أمثلة

يوضح كيفية استخراج الصفحات من المستند.

```csharp
// هناك عدة طرق لاستخراج الصفحات من المستند:
string doc = MyDir + "Big document.docx";

Splitter.ExtractPages(doc, ArtifactsDir + "LowCode.ExtractPages.1.docx", 0, 2);
Splitter.ExtractPages(doc, ArtifactsDir + "LowCode.ExtractPages.2.docx", SaveFormat.Docx, 0, 2);
```

### أنظر أيضا

* class [Splitter](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)

---

## ExtractPages(*string, string, [SaveFormat](../../../aspose.words/saveformat/), int, int*) {#extractpages_2}

يستخرج نطاقًا محددًا من الصفحات من ملف مستند ويحفظ الصفحات المستخرجة في ملف جديد باستخدام تنسيق الحفظ المحدد.

```csharp
public static void ExtractPages(string inputFileName, string outputFileName, SaveFormat saveFormat, 
    int startPageIndex, int pageCount)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| inputFileName | String | اسم ملف الإدخال. |
| outputFileName | String | اسم ملف الإخراج. |
| saveFormat | SaveFormat | تنسيق الحفظ. |
| startPageIndex | Int32 | الفهرس المبني على الصفر للصفحة الأولى التي سيتم استخراجها. |
| pageCount | Int32 | عدد الصفحات المطلوب استخراجها. |

## أمثلة

يوضح كيفية استخراج الصفحات من المستند.

```csharp
// هناك عدة طرق لاستخراج الصفحات من المستند:
string doc = MyDir + "Big document.docx";

Splitter.ExtractPages(doc, ArtifactsDir + "LowCode.ExtractPages.1.docx", 0, 2);
Splitter.ExtractPages(doc, ArtifactsDir + "LowCode.ExtractPages.2.docx", SaveFormat.Docx, 0, 2);
```

### أنظر أيضا

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Splitter](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)

---

## ExtractPages(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), int, int*) {#extractpages_3}

يستخرج نطاقًا محددًا من الصفحات من ملف مستند ويحفظ الصفحات المستخرجة في ملف جديد باستخدام تنسيق الحفظ المحدد.

```csharp
public static void ExtractPages(string inputFileName, string outputFileName, 
    SaveOptions saveOptions, int startPageIndex, int pageCount)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| inputFileName | String | اسم ملف الإدخال. |
| outputFileName | String | اسم ملف الإخراج. |
| saveOptions | SaveOptions | خيارات الحفظ. |
| startPageIndex | Int32 | الفهرس المبني على الصفر للصفحة الأولى التي سيتم استخراجها. |
| pageCount | Int32 | عدد الصفحات المطلوب استخراجها. |

### أنظر أيضا

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Splitter](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)

---

## ExtractPages(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), int, int*) {#extractpages}

يستخرج نطاقًا محددًا من الصفحات من مجرى مستند ويحفظ الصفحات المستخرجة في مجرى إخراج باستخدام تنسيق الحفظ المحدد.

```csharp
public static void ExtractPages(Stream inputStream, Stream outputStream, SaveFormat saveFormat, 
    int startPageIndex, int pageCount)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| inputStream | Stream | مجرى الإدخال. |
| outputStream | Stream | تيار الإخراج. |
| saveFormat | SaveFormat | تنسيق الحفظ. |
| startPageIndex | Int32 | الفهرس المبني على الصفر للصفحة الأولى التي سيتم استخراجها. |
| pageCount | Int32 | عدد الصفحات المطلوب استخراجها. |

## أمثلة

يوضح كيفية استخراج الصفحات من المستند من الدفق.

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ExtractPagesStream.docx", FileMode.Create, FileAccess.ReadWrite))
        Splitter.ExtractPages(streamIn, streamOut, SaveFormat.Docx, 0, 2);
}
```

### أنظر أيضا

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Splitter](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)

---

## ExtractPages(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), int, int*) {#extractpages_1}

يستخرج نطاقًا محددًا من الصفحات من مجرى مستند ويحفظ الصفحات المستخرجة في مجرى إخراج باستخدام تنسيق الحفظ المحدد.

```csharp
public static void ExtractPages(Stream inputStream, Stream outputStream, SaveOptions saveOptions, 
    int startPageIndex, int pageCount)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| inputStream | Stream | مجرى الإدخال. |
| outputStream | Stream | تيار الإخراج. |
| saveOptions | SaveOptions | خيارات الحفظ. |
| startPageIndex | Int32 | الفهرس المبني على الصفر للصفحة الأولى التي سيتم استخراجها. |
| pageCount | Int32 | عدد الصفحات المطلوب استخراجها. |

### أنظر أيضا

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Splitter](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)
