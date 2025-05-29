---
title: Comparer.Compare
linktitle: Compare
articleTitle: Compare
second_title: Aspose.Words لـ .NET
description: قارن مستندين بسهولة باستخدام طريقة المقارنة لدينا. احفظ الاختلافات، وتابع التعديلات، وراجع التنسيقات في ملف إخراج واحد.
type: docs
weight: 20
url: /ar/net/aspose.words.lowcode/comparer/compare/
---
## Compare(*string, string, string, string, DateTime, [CompareOptions](../../../aspose.words.comparing/compareoptions/)*) {#compare_4}

يقارن بين مستندين باستخدام خيارات إضافية ويحفظ الاختلافات في ملف الإخراج المحدد، ينتج تغييرات كعدد من مراجعات التحرير والتنسيق.

```csharp
public static void Compare(string v1, string v2, string outputFileName, string author, 
    DateTime dateTime, CompareOptions compareOptions = null)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| v1 | String | الوثيقة الأصلية. |
| v2 | String | الوثيقة المعدلة. |
| outputFileName | String | اسم ملف الإخراج. |
| author | String | الأحرف الأولى من اسم المؤلف لاستخدامها في المراجعات. |
| dateTime | DateTime | التاريخ والوقت المستخدم للمراجعة. |
| compareOptions | CompareOptions | خيارات مقارنة المستندات. |

## ملاحظات

إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، فسيتم حفظ كل صفحة من الإخراج كملف منفصل. سيتم استخدام اسم ملف الإخراج المحدد لإنشاء أسماء ملفات لكل جزء وفقًا للقاعدة: outputFile_partIndex.extension.

إذا كان تنسيق الإخراج هو TIFF، فسيتم حفظ الإخراج كملف TIFF متعدد الإطارات.

## أمثلة

يوضح كيفية مقارنة المستندات بطريقة بسيطة.

```csharp
// هناك عدة طرق لمقارنة المستندات:
string firstDoc = MyDir + "Table column bookmarks.docx";
string secondDoc = MyDir + "Table column bookmarks.doc";

Comparer.Compare(firstDoc, secondDoc, ArtifactsDir + "LowCode.CompareDocuments.1.docx", "Author", new DateTime());
Comparer.Compare(firstDoc, secondDoc, ArtifactsDir + "LowCode.CompareDocuments.2.docx", SaveFormat.Docx, "Author", new DateTime());

CompareOptions compareOptions = new CompareOptions();
compareOptions.IgnoreCaseChanges = true;
Comparer.Compare(firstDoc, secondDoc, ArtifactsDir + "LowCode.CompareDocuments.3.docx", "Author", new DateTime(), compareOptions);
Comparer.Compare(firstDoc, secondDoc, ArtifactsDir + "LowCode.CompareDocuments.4.docx", SaveFormat.Docx, "Author", new DateTime(), compareOptions);
```

### أنظر أيضا

* class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* class [Comparer](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)

---

## Compare(*string, string, string, [SaveFormat](../../../aspose.words/saveformat/), string, DateTime, [CompareOptions](../../../aspose.words.comparing/compareoptions/)*) {#compare_2}

يقارن بين مستندين باستخدام خيارات إضافية ويحفظ الاختلافات في ملف الإخراج المحدد بتنسيق الحفظ المقدم، ينتج تغييرات كعدد من مراجعات التحرير والتنسيق.

```csharp
public static void Compare(string v1, string v2, string outputFileName, SaveFormat saveFormat, 
    string author, DateTime dateTime, CompareOptions compareOptions = null)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| v1 | String | الوثيقة الأصلية. |
| v2 | String | الوثيقة المعدلة. |
| outputFileName | String | اسم ملف الإخراج. |
| saveFormat | SaveFormat | تنسيق حفظ الإخراج. |
| author | String | الأحرف الأولى من اسم المؤلف لاستخدامها في المراجعات. |
| dateTime | DateTime | التاريخ والوقت المستخدم للمراجعة. |
| compareOptions | CompareOptions | خيارات مقارنة المستندات. |

## ملاحظات

إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، فسيتم حفظ كل صفحة من الإخراج كملف منفصل. سيتم استخدام اسم ملف الإخراج المحدد لإنشاء أسماء ملفات لكل جزء وفقًا للقاعدة: outputFile_partIndex.extension.

إذا كان تنسيق الإخراج هو TIFF، فسيتم حفظ الإخراج كملف TIFF متعدد الإطارات.

## أمثلة

يوضح كيفية مقارنة المستندات بطريقة بسيطة.

```csharp
// هناك عدة طرق لمقارنة المستندات:
string firstDoc = MyDir + "Table column bookmarks.docx";
string secondDoc = MyDir + "Table column bookmarks.doc";

Comparer.Compare(firstDoc, secondDoc, ArtifactsDir + "LowCode.CompareDocuments.1.docx", "Author", new DateTime());
Comparer.Compare(firstDoc, secondDoc, ArtifactsDir + "LowCode.CompareDocuments.2.docx", SaveFormat.Docx, "Author", new DateTime());

CompareOptions compareOptions = new CompareOptions();
compareOptions.IgnoreCaseChanges = true;
Comparer.Compare(firstDoc, secondDoc, ArtifactsDir + "LowCode.CompareDocuments.3.docx", "Author", new DateTime(), compareOptions);
Comparer.Compare(firstDoc, secondDoc, ArtifactsDir + "LowCode.CompareDocuments.4.docx", SaveFormat.Docx, "Author", new DateTime(), compareOptions);
```

### أنظر أيضا

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* class [Comparer](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)

---

## Compare(*string, string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), string, DateTime, [CompareOptions](../../../aspose.words.comparing/compareoptions/)*) {#compare_3}

يقارن بين مستندين باستخدام خيارات إضافية ويحفظ الاختلافات في ملف الإخراج المحدد بتنسيق الحفظ المقدم، ينتج تغييرات كعدد من مراجعات التحرير والتنسيق.

```csharp
public static void Compare(string v1, string v2, string outputFileName, SaveOptions saveOptions, 
    string author, DateTime dateTime, CompareOptions compareOptions = null)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| v1 | String | الوثيقة الأصلية. |
| v2 | String | الوثيقة المعدلة. |
| outputFileName | String | اسم ملف الإخراج. |
| saveOptions | SaveOptions | خيارات حفظ الإخراج. |
| author | String | الأحرف الأولى من اسم المؤلف لاستخدامها في المراجعات. |
| dateTime | DateTime | التاريخ والوقت المستخدم للمراجعة. |
| compareOptions | CompareOptions | خيارات مقارنة المستندات. |

## ملاحظات

إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، فسيتم حفظ كل صفحة من الإخراج كملف منفصل. سيتم استخدام اسم ملف الإخراج المحدد لإنشاء أسماء ملفات لكل جزء وفقًا للقاعدة: outputFile_partIndex.extension.

إذا كان تنسيق الإخراج هو TIFF، فسيتم حفظ الإخراج كملف TIFF متعدد الإطارات.

### أنظر أيضا

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* class [Comparer](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)

---

## Compare(*Stream, Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), string, DateTime, [CompareOptions](../../../aspose.words.comparing/compareoptions/)*) {#compare}

يقارن بين مستندين تم تحميلهما من تدفقات تحتوي على خيارات إضافية ويحفظ الاختلافات في تدفق الإخراج المقدم بتنسيق الحفظ المحدد، ينتج تغييرات كعدد من مراجعات التحرير والتنسيق.

```csharp
public static void Compare(Stream v1, Stream v2, Stream outputStream, SaveFormat saveFormat, 
    string author, DateTime dateTime, CompareOptions compareOptions = null)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| v1 | Stream | الوثيقة الأصلية. |
| v2 | Stream | الوثيقة المعدلة. |
| outputStream | Stream | تيار الإخراج. |
| saveFormat | SaveFormat | تنسيق حفظ الإخراج. |
| author | String | الأحرف الأولى من اسم المؤلف لاستخدامها في المراجعات. |
| dateTime | DateTime | التاريخ والوقت المستخدم للمراجعة. |
| compareOptions | CompareOptions | خيارات مقارنة المستندات. |

## ملاحظات

إذا كان تنسيق الإخراج عبارة عن صورة (BMP، أو EMF، أو EPS، أو GIF، أو JPEG، أو PNG، أو WebP)، فسيتم حفظ الصفحة الأولى فقط من الإخراج في التدفق المحدد.

إذا كان تنسيق الإخراج هو TIFF، فسيتم حفظ الإخراج كملف TIFF متعدد الإطارات إلى الدفق المحدد.

## أمثلة

يوضح كيفية مقارنة المستندات من التدفق.

```csharp
// هناك عدة طرق لمقارنة المستندات من التدفق:
using (FileStream firstStreamIn = new FileStream(MyDir + "Table column bookmarks.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(MyDir + "Table column bookmarks.doc", FileMode.Open, FileAccess.Read))
    {
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.CompareStreamDocuments.1.docx", FileMode.Create, FileAccess.ReadWrite))
            Comparer.Compare(firstStreamIn, secondStreamIn, streamOut, SaveFormat.Docx, "Author", new DateTime());

        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.CompareStreamDocuments.2.docx", FileMode.Create, FileAccess.ReadWrite))
        {
            CompareOptions compareOptions = new CompareOptions();
            compareOptions.IgnoreCaseChanges = true;
            Comparer.Compare(firstStreamIn, secondStreamIn, streamOut, SaveFormat.Docx, "Author", new DateTime(), compareOptions);
        }
    }
}
```

### أنظر أيضا

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* class [Comparer](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)

---

## Compare(*Stream, Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), string, DateTime, [CompareOptions](../../../aspose.words.comparing/compareoptions/)*) {#compare_1}

يقارن بين مستندين تم تحميلهما من تدفقات تحتوي على خيارات إضافية ويحفظ الاختلافات في تدفق الإخراج المقدم بتنسيق الحفظ المحدد، ينتج تغييرات كعدد من مراجعات التحرير والتنسيق.

```csharp
public static void Compare(Stream v1, Stream v2, Stream outputStream, SaveOptions saveOptions, 
    string author, DateTime dateTime, CompareOptions compareOptions = null)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| v1 | Stream | الوثيقة الأصلية. |
| v2 | Stream | الوثيقة المعدلة. |
| outputStream | Stream | تيار الإخراج. |
| saveOptions | SaveOptions | خيارات حفظ الإخراج. |
| author | String | الأحرف الأولى من اسم المؤلف لاستخدامها في المراجعات. |
| dateTime | DateTime | التاريخ والوقت المستخدم للمراجعة. |
| compareOptions | CompareOptions | خيارات مقارنة المستندات. |

## ملاحظات

إذا كان تنسيق الإخراج عبارة عن صورة (BMP، أو EMF، أو EPS، أو GIF، أو JPEG، أو PNG، أو WebP)، فسيتم حفظ الصفحة الأولى فقط من الإخراج في التدفق المحدد.

إذا كان تنسيق الإخراج هو TIFF، فسيتم حفظ الإخراج كملف TIFF متعدد الإطارات إلى الدفق المحدد.

### أنظر أيضا

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* class [Comparer](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)
