---
title: Watermarker.SetText
linktitle: SetText
articleTitle: SetText
second_title: Aspose.Words لـ .NET
description: حسّن مستنداتك باستخدام أسلوبنا لإضافة علامات مائية نصية. أضف علامات مائية نصية قابلة للتخصيص بسهولة لتحسين هوية العلامة التجارية واحترافيتها.
type: docs
weight: 30
url: /ar/net/aspose.words.lowcode/watermarker/settext/
---
## SetText(*string, string, string*) {#settext_4}

يضيف علامة مائية نصية إلى المستند.

```csharp
public static void SetText(string inputFileName, string outputFileName, string watermarkText)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| inputFileName | String | اسم ملف الإدخال. |
| outputFileName | String | اسم ملف الإخراج. |
| watermarkText | String | النص الذي يتم عرضه كعلامة مائية. |

## ملاحظات

إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، فسيتم حفظ كل صفحة من الإخراج كملف منفصل. سيتم استخدام اسم ملف الإخراج المحدد لإنشاء أسماء ملفات لكل جزء وفقًا للقاعدة: outputFile_partIndex.extension.

إذا كان تنسيق الإخراج هو TIFF، فسيتم حفظ الإخراج كملف TIFF متعدد الإطارات.

## أمثلة

يوضح كيفية إدراج نص العلامة المائية في المستند.

```csharp
string doc = MyDir + "Big document.docx";
string watermarkText = "This is a watermark";

Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.1.docx", watermarkText);
Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.2.docx", SaveFormat.Docx, watermarkText);
TextWatermarkOptions watermarkOptions = new TextWatermarkOptions();
watermarkOptions.Color = Color.Red;
Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.3.docx", watermarkText, watermarkOptions);
Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.4.docx", SaveFormat.Docx, watermarkText, watermarkOptions);
```

### أنظر أيضا

* class [Watermarker](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)

---

## SetText(*string, string, string, [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)*) {#settext_5}

يضيف علامة مائية نصية إلى المستند باستخدام الخيارات.

```csharp
public static void SetText(string inputFileName, string outputFileName, string watermarkText, 
    TextWatermarkOptions options)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| inputFileName | String | اسم ملف الإدخال. |
| outputFileName | String | اسم ملف الإخراج. |
| watermarkText | String | النص الذي يتم عرضه كعلامة مائية. |
| options | TextWatermarkOptions | يحدد خيارات إضافية للعلامة المائية النصية. |

## ملاحظات

إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، فسيتم حفظ كل صفحة من الإخراج كملف منفصل. سيتم استخدام اسم ملف الإخراج المحدد لإنشاء أسماء ملفات لكل جزء وفقًا للقاعدة: outputFile_partIndex.extension.

إذا كان تنسيق الإخراج هو TIFF، فسيتم حفظ الإخراج كملف TIFF متعدد الإطارات.

## أمثلة

يوضح كيفية إدراج نص العلامة المائية في المستند.

```csharp
string doc = MyDir + "Big document.docx";
string watermarkText = "This is a watermark";

Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.1.docx", watermarkText);
Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.2.docx", SaveFormat.Docx, watermarkText);
TextWatermarkOptions watermarkOptions = new TextWatermarkOptions();
watermarkOptions.Color = Color.Red;
Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.3.docx", watermarkText, watermarkOptions);
Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.4.docx", SaveFormat.Docx, watermarkText, watermarkOptions);
```

### أنظر أيضا

* class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* class [Watermarker](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)

---

## SetText(*string, string, [SaveFormat](../../../aspose.words/saveformat/), string, [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)*) {#settext_2}

يضيف علامة مائية نصية إلى المستند مع خيارات وتنسيق حفظ محدد.

```csharp
public static void SetText(string inputFileName, string outputFileName, SaveFormat saveFormat, 
    string watermarkText, TextWatermarkOptions options = null)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| inputFileName | String | اسم ملف الإدخال. |
| outputFileName | String | اسم ملف الإخراج. |
| saveFormat | SaveFormat | تنسيق الحفظ. |
| watermarkText | String | النص الذي يتم عرضه كعلامة مائية. |
| options | TextWatermarkOptions | يحدد خيارات إضافية للعلامة المائية النصية. |

## ملاحظات

إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، فسيتم حفظ كل صفحة من الإخراج كملف منفصل. سيتم استخدام اسم ملف الإخراج المحدد لإنشاء أسماء ملفات لكل جزء وفقًا للقاعدة: outputFile_partIndex.extension.

إذا كان تنسيق الإخراج هو TIFF، فسيتم حفظ الإخراج كملف TIFF متعدد الإطارات.

## أمثلة

يوضح كيفية إدراج نص العلامة المائية في المستند.

```csharp
string doc = MyDir + "Big document.docx";
string watermarkText = "This is a watermark";

Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.1.docx", watermarkText);
Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.2.docx", SaveFormat.Docx, watermarkText);
TextWatermarkOptions watermarkOptions = new TextWatermarkOptions();
watermarkOptions.Color = Color.Red;
Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.3.docx", watermarkText, watermarkOptions);
Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.4.docx", SaveFormat.Docx, watermarkText, watermarkOptions);
```

### أنظر أيضا

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* class [Watermarker](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)

---

## SetText(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), string, [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)*) {#settext_3}

يضيف علامة مائية نصية إلى المستند مع خيارات وتنسيق حفظ محدد.

```csharp
public static void SetText(string inputFileName, string outputFileName, SaveOptions saveOptions, 
    string watermarkText, TextWatermarkOptions options = null)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| inputFileName | String | اسم ملف الإدخال. |
| outputFileName | String | اسم ملف الإخراج. |
| saveOptions | SaveOptions | خيارات الحفظ. |
| watermarkText | String | النص الذي يتم عرضه كعلامة مائية. |
| options | TextWatermarkOptions | يحدد خيارات إضافية للعلامة المائية النصية. |

## ملاحظات

إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، فسيتم حفظ كل صفحة من الإخراج كملف منفصل. سيتم استخدام اسم ملف الإخراج المحدد لإنشاء أسماء ملفات لكل جزء وفقًا للقاعدة: outputFile_partIndex.extension.

إذا كان تنسيق الإخراج هو TIFF، فسيتم حفظ الإخراج كملف TIFF متعدد الإطارات.

### أنظر أيضا

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* class [Watermarker](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)

---

## SetText(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), string, [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)*) {#settext}

يضيف علامة مائية نصية إلى المستند من التدفقات التي تحتوي على خيارات.

```csharp
public static void SetText(Stream inputStream, Stream outputStream, SaveFormat saveFormat, 
    string watermarkText, TextWatermarkOptions options = null)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| inputStream | Stream | مجرى الإدخال. |
| outputStream | Stream | تيار الإخراج. |
| saveFormat | SaveFormat | تنسيق الحفظ. |
| watermarkText | String | النص الذي يتم عرضه كعلامة مائية. |
| options | TextWatermarkOptions | يحدد خيارات إضافية للعلامة المائية النصية. |

## ملاحظات

إذا كان تنسيق الإخراج عبارة عن صورة (BMP، أو EMF، أو EPS، أو GIF، أو JPEG، أو PNG، أو WebP)، فسيتم حفظ الصفحة الأولى فقط من الإخراج في التدفق المحدد.

إذا كان تنسيق الإخراج هو TIFF، فسيتم حفظ الإخراج كملف TIFF متعدد الإطارات إلى الدفق المحدد.

## أمثلة

يوضح كيفية إدراج نص العلامة المائية في المستند من الدفق.

```csharp
string watermarkText = "This is a watermark";

using (FileStream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.WatermarkTextStream.1.docx", FileMode.Create, FileAccess.ReadWrite))
        Watermarker.SetText(streamIn, streamOut, SaveFormat.Docx, watermarkText);

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.WatermarkTextStream.2.docx", FileMode.Create, FileAccess.ReadWrite))
    {
        TextWatermarkOptions options = new TextWatermarkOptions();
        options.Color = Color.Red;
        Watermarker.SetText(streamIn, streamOut, SaveFormat.Docx, watermarkText, options);
    }
}
```

### أنظر أيضا

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* class [Watermarker](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)

---

## SetText(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), string, [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)*) {#settext_1}

يضيف علامة مائية نصية إلى المستند من التدفقات التي تحتوي على خيارات.

```csharp
public static void SetText(Stream inputStream, Stream outputStream, SaveOptions saveOptions, 
    string watermarkText, TextWatermarkOptions options = null)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| inputStream | Stream | مجرى الإدخال. |
| outputStream | Stream | تيار الإخراج. |
| saveOptions | SaveOptions | خيارات الحفظ. |
| watermarkText | String | النص الذي يتم عرضه كعلامة مائية. |
| options | TextWatermarkOptions | يحدد خيارات إضافية للعلامة المائية النصية. |

## ملاحظات

إذا كان تنسيق الإخراج عبارة عن صورة (BMP، أو EMF، أو EPS، أو GIF، أو JPEG، أو PNG، أو WebP)، فسيتم حفظ الصفحة الأولى فقط من الإخراج في التدفق المحدد.

إذا كان تنسيق الإخراج هو TIFF، فسيتم حفظ الإخراج كملف TIFF متعدد الإطارات إلى الدفق المحدد.

### أنظر أيضا

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* class [Watermarker](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)
