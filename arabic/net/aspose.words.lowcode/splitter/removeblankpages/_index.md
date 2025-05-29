---
title: Splitter.RemoveBlankPages
linktitle: RemoveBlankPages
articleTitle: RemoveBlankPages
second_title: Aspose.Words لـ .NET
description: تخلص من الصفحات الفارغة بسهولة من مستنداتك باستخدام طريقة Splitter RemoveBlankPages. وفر وقتك وحسّن سير عملك اليوم!
type: docs
weight: 30
url: /ar/net/aspose.words.lowcode/splitter/removeblankpages/
---
## RemoveBlankPages(*string, string*) {#removeblankpages_2}

يزيل الصفحات الفارغة من المستند ويحفظ النتيجة. يُرجع قائمة بأرقام الصفحات التي تمت إزالتها.

```csharp
public static List<int> RemoveBlankPages(string inputFileName, string outputFileName)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| inputFileName | String | اسم ملف الإدخال. |
| outputFileName | String | اسم ملف الإخراج. |

### قيمة الإرجاع

لقد تم اعتبار قائمة أرقام الصفحات فارغة وتم إزالتها.

## أمثلة

يوضح كيفية إزالة الصفحات الفارغة من المستند.

```csharp
// هناك عدة طرق لإزالة الصفحات الفارغة من المستند:
string doc = MyDir + "Blank pages.docx";

Splitter.RemoveBlankPages(doc, ArtifactsDir + "LowCode.RemoveBlankPages.1.docx");
Splitter.RemoveBlankPages(doc, ArtifactsDir + "LowCode.RemoveBlankPages.2.docx", SaveFormat.Docx);
```

### أنظر أيضا

* class [Splitter](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)

---

## RemoveBlankPages(*string, string, [SaveFormat](../../../aspose.words/saveformat/)*) {#removeblankpages_3}

يزيل الصفحات الفارغة من المستند ويحفظ الناتج بالتنسيق المحدد. يُرجع قائمة بأرقام الصفحات التي تمت إزالتها.

```csharp
public static List<int> RemoveBlankPages(string inputFileName, string outputFileName, 
    SaveFormat saveFormat)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| inputFileName | String | اسم ملف الإدخال. |
| outputFileName | String | اسم ملف الإخراج. |
| saveFormat | SaveFormat | تنسيق الحفظ. |

### قيمة الإرجاع

لقد تم اعتبار قائمة أرقام الصفحات فارغة وتم إزالتها.

## أمثلة

يوضح كيفية إزالة الصفحات الفارغة من المستند.

```csharp
// هناك عدة طرق لإزالة الصفحات الفارغة من المستند:
string doc = MyDir + "Blank pages.docx";

Splitter.RemoveBlankPages(doc, ArtifactsDir + "LowCode.RemoveBlankPages.1.docx");
Splitter.RemoveBlankPages(doc, ArtifactsDir + "LowCode.RemoveBlankPages.2.docx", SaveFormat.Docx);
```

### أنظر أيضا

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Splitter](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)

---

## RemoveBlankPages(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#removeblankpages_4}

يزيل الصفحات الفارغة من المستند ويحفظ الناتج بالتنسيق المحدد. يُرجع قائمة بأرقام الصفحات التي تمت إزالتها.

```csharp
public static List<int> RemoveBlankPages(string inputFileName, string outputFileName, 
    SaveOptions saveOptions)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| inputFileName | String | اسم ملف الإدخال. |
| outputFileName | String | اسم ملف الإخراج. |
| saveOptions | SaveOptions | خيارات الحفظ. |

### قيمة الإرجاع

لقد تم اعتبار قائمة أرقام الصفحات فارغة وتم إزالتها.

### أنظر أيضا

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Splitter](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)

---

## RemoveBlankPages(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/)*) {#removeblankpages}

يزيل الصفحات الفارغة من مستند مُقدَّم في مسار إدخال، ويحفظ المستند المُحدَّث في مسار إخراج بتنسيق الحفظ المُحدَّد. يُرجع قائمة بأرقام الصفحات التي حُذفت.

```csharp
public static List<int> RemoveBlankPages(Stream inputStream, Stream outputStream, 
    SaveFormat saveFormat)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| inputStream | Stream | مجرى الإدخال. |
| outputStream | Stream | تيار الإخراج. |
| saveFormat | SaveFormat | تنسيق الحفظ. |

### قيمة الإرجاع

لقد تم اعتبار قائمة أرقام الصفحات فارغة وتم إزالتها.

## أمثلة

يوضح كيفية إزالة الصفحات الفارغة من المستند من التدفق.

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Blank pages.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.RemoveBlankPagesStream.docx", FileMode.Create, FileAccess.ReadWrite))
        Splitter.RemoveBlankPages(streamIn, streamOut, SaveFormat.Docx);
}
```

### أنظر أيضا

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Splitter](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)

---

## RemoveBlankPages(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#removeblankpages_1}

يزيل الصفحات الفارغة من مستند مُقدَّم في مسار إدخال، ويحفظ المستند المُحدَّث في مسار إخراج بتنسيق الحفظ المُحدَّد. يُرجع قائمة بأرقام الصفحات التي حُذفت.

```csharp
public static List<int> RemoveBlankPages(Stream inputStream, Stream outputStream, 
    SaveOptions saveOptions)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| inputStream | Stream | مجرى الإدخال. |
| outputStream | Stream | تيار الإخراج. |
| saveOptions | SaveOptions | خيارات الحفظ. |

### قيمة الإرجاع

لقد تم اعتبار قائمة أرقام الصفحات فارغة وتم إزالتها.

### أنظر أيضا

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Splitter](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)
