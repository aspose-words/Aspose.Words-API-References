---
title: Splitter.Split
linktitle: Split
articleTitle: Split
second_title: Aspose.Words لـ .NET
description: قسّم مستنداتك بسهولة إلى عدة أقسام باستخدام طريقة Splitter Split المرنة. احفظها بتنسيقك المفضل لإدارة ملفاتك بسهولة!
type: docs
weight: 40
url: /ar/net/aspose.words.lowcode/splitter/split/
---
## Split(*string, string, [SplitOptions](../../splitoptions/)*) {#split_2}

يُقسّم المستند إلى أجزاء متعددة بناءً على خيارات التقسيم المُحددة، ويحفظ الأجزاء الناتجة في ملفات. يُحدَّد تنسيق ملف الإخراج بناءً على امتداد اسم ملف الإخراج.

```csharp
public static void Split(string inputFileName, string outputFileName, SplitOptions options)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| inputFileName | String | اسم ملف الإدخال. |
| outputFileName | String | اسم ملف الإخراج المستخدم لإنشاء اسم الملف لأجزاء المستند باستخدام القاعدة "outputFile_partIndex.extension" |
| options | SplitOptions | خيارات تقسيم المستند. |

## أمثلة

يوضح كيفية تقسيم المستند حسب الصفحات.

```csharp
string doc = MyDir + "Big document.docx";

SplitOptions options = new SplitOptions();
options.SplitCriteria = SplitCriteria.Page;
Splitter.Split(doc, ArtifactsDir + "LowCode.SplitDocument.1.docx", options);
Splitter.Split(doc, ArtifactsDir + "LowCode.SplitDocument.2.docx", SaveFormat.Docx, options);
```

### أنظر أيضا

* class [SplitOptions](../../splitoptions/)
* class [Splitter](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)

---

## Split(*string, string, [SaveFormat](../../../aspose.words/saveformat/), [SplitOptions](../../splitoptions/)*) {#split_3}

يقسم المستند إلى أجزاء متعددة استنادًا إلى خيارات التقسيم المحددة ويحفظ الأجزاء الناتجة في ملفات بتنسيق الحفظ المحدد.

```csharp
public static void Split(string inputFileName, string outputFileName, SaveFormat saveFormat, 
    SplitOptions options)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| inputFileName | String | اسم ملف الإدخال. |
| outputFileName | String | اسم ملف الإخراج المستخدم لإنشاء اسم الملف لأجزاء المستند باستخدام القاعدة "outputFile_partIndex.extension" |
| saveFormat | SaveFormat | تنسيق الحفظ. |
| options | SplitOptions | خيارات تقسيم المستند. |

## أمثلة

يوضح كيفية تقسيم المستند حسب الصفحات.

```csharp
string doc = MyDir + "Big document.docx";

SplitOptions options = new SplitOptions();
options.SplitCriteria = SplitCriteria.Page;
Splitter.Split(doc, ArtifactsDir + "LowCode.SplitDocument.1.docx", options);
Splitter.Split(doc, ArtifactsDir + "LowCode.SplitDocument.2.docx", SaveFormat.Docx, options);
```

### أنظر أيضا

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [SplitOptions](../../splitoptions/)
* class [Splitter](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)

---

## Split(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), [SplitOptions](../../splitoptions/)*) {#split_4}

يقسم المستند إلى أجزاء متعددة استنادًا إلى خيارات التقسيم المحددة ويحفظ الأجزاء الناتجة في ملفات بتنسيق الحفظ المحدد.

```csharp
public static void Split(string inputFileName, string outputFileName, SaveOptions saveOptions, 
    SplitOptions options)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| inputFileName | String | اسم ملف الإدخال. |
| outputFileName | String | اسم ملف الإخراج المستخدم لإنشاء اسم الملف لأجزاء المستند باستخدام القاعدة "outputFile_partIndex.extension" |
| saveOptions | SaveOptions | خيارات الحفظ. |
| options | SplitOptions | خيارات تقسيم المستند. |

### أنظر أيضا

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [SplitOptions](../../splitoptions/)
* class [Splitter](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)

---

## Split(*Stream, [SaveFormat](../../../aspose.words/saveformat/), [SplitOptions](../../splitoptions/)*) {#split}

يقوم بتقسيم مستند من مجرى إدخال إلى أجزاء متعددة استنادًا إلى خيارات التقسيم المحددة ويقوم بإرجاع الأجزاء الناتجة كمجموعة من المجاري بتنسيق الحفظ المحدد.

```csharp
public static Stream[] Split(Stream inputStream, SaveFormat saveFormat, SplitOptions options)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| inputStream | Stream | مجرى الإدخال. |
| saveFormat | SaveFormat | تنسيق الحفظ. |
| options | SplitOptions | خيارات تقسيم المستند. |

## أمثلة

يوضح كيفية تقسيم المستند من التدفق حسب الصفحات.

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    SplitOptions options = new SplitOptions();
    options.SplitCriteria = SplitCriteria.Page;
    Stream[] stream = Splitter.Split(streamIn, SaveFormat.Docx, options);
}
```

### أنظر أيضا

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [SplitOptions](../../splitoptions/)
* class [Splitter](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)

---

## Split(*Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), [SplitOptions](../../splitoptions/)*) {#split_1}

يقوم بتقسيم مستند من مجرى إدخال إلى أجزاء متعددة استنادًا إلى خيارات التقسيم المحددة ويقوم بإرجاع الأجزاء الناتجة كمجموعة من المجاري بتنسيق الحفظ المحدد.

```csharp
public static Stream[] Split(Stream inputStream, SaveOptions saveOptions, SplitOptions options)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| inputStream | Stream | مجرى الإدخال. |
| saveOptions | SaveOptions | خيارات الحفظ. |
| options | SplitOptions | خيارات تقسيم المستند. |

### أنظر أيضا

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [SplitOptions](../../splitoptions/)
* class [Splitter](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)
