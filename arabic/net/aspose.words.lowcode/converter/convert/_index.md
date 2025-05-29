---
title: Converter.Convert
linktitle: Convert
articleTitle: Convert
second_title: Aspose.Words لـ .NET
description: حوّل مستنداتك بسهولة باستخدام طريقة التحويل في برنامجنا. حوّل ملفات الإدخال إلى التنسيقات المطلوبة بسهولة ودقة.
type: docs
weight: 20
url: /ar/net/aspose.words.lowcode/converter/convert/
---
## Convert(*string, string*) {#convert_4}

يحول مستند الإدخال المعطى إلى مستند الإخراج باستخدام أسماء ملفات الإدخال والإخراج المحددة وملحقاتها.

```csharp
public static void Convert(string inputFile, string outputFile)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| inputFile | String | اسم ملف الإدخال. |
| outputFile | String | اسم ملف الإخراج. |

## ملاحظات

إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، فسيتم حفظ كل صفحة من الإخراج كملف منفصل. سيتم استخدام اسم ملف الإخراج المحدد لإنشاء أسماء ملفات لكل جزء وفقًا للقاعدة: outputFile_partIndex.extension.

إذا كان تنسيق الإخراج هو TIFF، فسيتم حفظ الإخراج كملف TIFF متعدد الإطارات.

## أمثلة

يوضح كيفية تحويل المستندات بسطر واحد من التعليمات البرمجية.

```csharp
string doc = MyDir + "Document.docx";

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.pdf");

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.SaveFormat.rtf", SaveFormat.Rtf);

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
Converter.Convert(doc, loadOptions, ArtifactsDir + "LowCode.Convert.LoadOptions.docx", saveOptions);

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.SaveOptions.docx", saveOptions);
```

### أنظر أيضا

* class [Converter](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)

---

## Convert(*string, string, [SaveFormat](../../../aspose.words/saveformat/)*) {#convert_5}

يحول مستند الإدخال المعطى إلى مستند الإخراج باستخدام أسماء ملفات الإدخال والإخراج المحددة وتنسيق المستند النهائي.

```csharp
public static void Convert(string inputFile, string outputFile, SaveFormat saveFormat)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| inputFile | String | اسم ملف الإدخال. |
| outputFile | String | اسم ملف الإخراج. |
| saveFormat | SaveFormat | تنسيق الحفظ. |

## ملاحظات

إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، فسيتم حفظ كل صفحة من الإخراج كملف منفصل. سيتم استخدام اسم ملف الإخراج المحدد لإنشاء أسماء ملفات لكل جزء وفقًا للقاعدة: outputFile_partIndex.extension.

إذا كان تنسيق الإخراج هو TIFF، فسيتم حفظ الإخراج كملف TIFF متعدد الإطارات.

## أمثلة

يوضح كيفية تحويل المستندات بسطر واحد من التعليمات البرمجية.

```csharp
string doc = MyDir + "Document.docx";

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.pdf");

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.SaveFormat.rtf", SaveFormat.Rtf);

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
Converter.Convert(doc, loadOptions, ArtifactsDir + "LowCode.Convert.LoadOptions.docx", saveOptions);

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.SaveOptions.docx", saveOptions);
```

### أنظر أيضا

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Converter](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)

---

## Convert(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#convert_6}

يحول مستند الإدخال المعطى إلى مستند الإخراج باستخدام أسماء ملفات الإدخال والإخراج المحددة وخيارات الحفظ.

```csharp
public static void Convert(string inputFile, string outputFile, SaveOptions saveOptions)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| inputFile | String | اسم ملف الإدخال. |
| outputFile | String | اسم ملف الإخراج. |
| saveOptions | SaveOptions | خيارات الحفظ. |

## ملاحظات

إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، فسيتم حفظ كل صفحة من الإخراج كملف منفصل. سيتم استخدام اسم ملف الإخراج المحدد لإنشاء أسماء ملفات لكل جزء وفقًا للقاعدة: outputFile_partIndex.extension.

إذا كان تنسيق الإخراج هو TIFF، فسيتم حفظ الإخراج كملف TIFF متعدد الإطارات.

## أمثلة

يوضح كيفية تحويل المستندات بسطر واحد من التعليمات البرمجية.

```csharp
string doc = MyDir + "Document.docx";

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.pdf");

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.SaveFormat.rtf", SaveFormat.Rtf);

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
Converter.Convert(doc, loadOptions, ArtifactsDir + "LowCode.Convert.LoadOptions.docx", saveOptions);

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.SaveOptions.docx", saveOptions);
```

### أنظر أيضا

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Converter](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)

---

## Convert(*string, [LoadOptions](../../../aspose.words.loading/loadoptions/), string, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#convert_3}

يحول مستند الإدخال المعطى إلى مستند الإخراج باستخدام أسماء ملفات الإدخال والإخراج المحددة وخيارات التحميل/الحفظ الخاصة به.

```csharp
public static void Convert(string inputFile, LoadOptions loadOptions, string outputFile, 
    SaveOptions saveOptions)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| inputFile | String | اسم ملف الإدخال. |
| loadOptions | LoadOptions | خيارات تحميل مستند الإدخال. |
| outputFile | String | اسم ملف الإخراج. |
| saveOptions | SaveOptions | خيارات الحفظ. |

## ملاحظات

إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، فسيتم حفظ كل صفحة من الإخراج كملف منفصل. سيتم استخدام اسم ملف الإخراج المحدد لإنشاء أسماء ملفات لكل جزء وفقًا للقاعدة: outputFile_partIndex.extension.

إذا كان تنسيق الإخراج هو TIFF، فسيتم حفظ الإخراج كملف TIFF متعدد الإطارات.

## أمثلة

يوضح كيفية تحويل المستندات بسطر واحد من التعليمات البرمجية.

```csharp
string doc = MyDir + "Document.docx";

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.pdf");

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.SaveFormat.rtf", SaveFormat.Rtf);

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
Converter.Convert(doc, loadOptions, ArtifactsDir + "LowCode.Convert.LoadOptions.docx", saveOptions);

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.SaveOptions.docx", saveOptions);
```

### أنظر أيضا

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Converter](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)

---

## Convert(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/)*) {#convert_1}

يحول مستند الإدخال المعطى إلى مستند إخراج واحد باستخدام تدفقات الإدخال والإخراج المحددة.

```csharp
public static void Convert(Stream inputStream, Stream outputStream, SaveFormat saveFormat)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| inputStream | Stream | مجرى الإدخال. |
| outputStream | Stream | تيار الإخراج. |
| saveFormat | SaveFormat | تنسيق الحفظ. |

## ملاحظات

إذا كان تنسيق الإخراج عبارة عن صورة (BMP، أو EMF، أو EPS، أو GIF، أو JPEG، أو PNG، أو WebP)، فسيتم حفظ الصفحة الأولى فقط من الإخراج في التدفق المحدد.

إذا كان تنسيق الإخراج هو TIFF، فسيتم حفظ الإخراج كملف TIFF متعدد الإطارات إلى الدفق المحدد.

## أمثلة

يوضح كيفية تحويل المستندات باستخدام سطر واحد من التعليمات البرمجية (Stream).

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertStream.1.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Convert(streamIn, streamOut, SaveFormat.Docx);

    OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
    LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertStream.2.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Convert(streamIn, loadOptions, streamOut, saveOptions);

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertStream.3.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Convert(streamIn, streamOut, saveOptions);
}
```

### أنظر أيضا

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Converter](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)

---

## Convert(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#convert_2}

يحول مستند الإدخال المعطى إلى مستند إخراج واحد باستخدام تدفقات الإدخال والإخراج المحددة.

```csharp
public static void Convert(Stream inputStream, Stream outputStream, SaveOptions saveOptions)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| inputStream | Stream | تدفقات الإدخال. |
| outputStream | Stream | تيار الإخراج. |
| saveOptions | SaveOptions | خيارات الحفظ. |

## ملاحظات

إذا كان تنسيق الإخراج عبارة عن صورة (BMP، أو EMF، أو EPS، أو GIF، أو JPEG، أو PNG، أو WebP)، فسيتم حفظ الصفحة الأولى فقط من الإخراج في التدفق المحدد.

إذا كان تنسيق الإخراج هو TIFF، فسيتم حفظ الإخراج كملف TIFF متعدد الإطارات إلى الدفق المحدد.

## أمثلة

يوضح كيفية تحويل المستندات باستخدام سطر واحد من التعليمات البرمجية (Stream).

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertStream.1.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Convert(streamIn, streamOut, SaveFormat.Docx);

    OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
    LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertStream.2.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Convert(streamIn, loadOptions, streamOut, saveOptions);

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertStream.3.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Convert(streamIn, streamOut, saveOptions);
}
```

### أنظر أيضا

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Converter](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)

---

## Convert(*Stream, [LoadOptions](../../../aspose.words.loading/loadoptions/), Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#convert}

يحول مستند الإدخال المعطى إلى مستند إخراج واحد باستخدام تدفقات الإدخال والإخراج المحددة.

```csharp
public static void Convert(Stream inputStream, LoadOptions loadOptions, Stream outputStream, 
    SaveOptions saveOptions)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| inputStream | Stream | تدفقات الإدخال. |
| loadOptions | LoadOptions | خيارات تحميل مستند الإدخال. |
| outputStream | Stream | تيار الإخراج. |
| saveOptions | SaveOptions | خيارات الحفظ. |

## ملاحظات

إذا كان تنسيق الإخراج عبارة عن صورة (BMP، أو EMF، أو EPS، أو GIF، أو JPEG، أو PNG، أو WebP)، فسيتم حفظ الصفحة الأولى فقط من الإخراج في التدفق المحدد.

إذا كان تنسيق الإخراج هو TIFF، فسيتم حفظ الإخراج كملف TIFF متعدد الإطارات إلى الدفق المحدد.

## أمثلة

يوضح كيفية تحويل المستندات باستخدام سطر واحد من التعليمات البرمجية (Stream).

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertStream.1.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Convert(streamIn, streamOut, SaveFormat.Docx);

    OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
    LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertStream.2.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Convert(streamIn, loadOptions, streamOut, saveOptions);

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertStream.3.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Convert(streamIn, streamOut, saveOptions);
}
```

### أنظر أيضا

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Converter](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)
