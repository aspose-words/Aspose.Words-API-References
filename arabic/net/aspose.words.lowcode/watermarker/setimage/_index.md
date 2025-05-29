---
title: Watermarker.SetImage
linktitle: SetImage
articleTitle: SetImage
second_title: Aspose.Words لـ .NET
description: أضف علامات مائية مخصصة لصورك بسهولة لإضفاء لمسة احترافية على مستنداتك باستخدام أداة Watermarker SetImage.
type: docs
weight: 20
url: /ar/net/aspose.words.lowcode/watermarker/setimage/
---
## SetImage(*string, string, string*) {#setimage_6}

يضيف علامة مائية للصورة إلى المستند.

```csharp
public static void SetImage(string inputFileName, string outputFileName, 
    string watermarkImageFileName)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| inputFileName | String | اسم ملف الإدخال. |
| outputFileName | String | اسم ملف الإخراج. |
| watermarkImageFileName | String | صورة يتم عرضها كعلامة مائية. |

## ملاحظات

إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، فسيتم حفظ كل صفحة من الإخراج كملف منفصل. سيتم استخدام اسم ملف الإخراج المحدد لإنشاء أسماء ملفات لكل جزء وفقًا للقاعدة: outputFile_partIndex.extension.

إذا كان تنسيق الإخراج هو TIFF، فسيتم حفظ الإخراج كملف TIFF متعدد الإطارات.

## أمثلة

يوضح كيفية إدراج صورة العلامة المائية في المستند.

```csharp
string doc = MyDir + "Document.docx";
string watermarkImage = ImageDir + "Logo.jpg";

Watermarker.SetImage(doc, ArtifactsDir + "LowCode.SetWatermarkImage.1.docx", watermarkImage);
Watermarker.SetImage(doc, ArtifactsDir + "LowCode.SetWatermarkText.2.docx", SaveFormat.Docx, watermarkImage);

ImageWatermarkOptions options = new ImageWatermarkOptions();
options.Scale = 50;
Watermarker.SetImage(doc, ArtifactsDir + "LowCode.SetWatermarkText.3.docx", watermarkImage, options);
Watermarker.SetImage(doc, ArtifactsDir + "LowCode.SetWatermarkText.4.docx", SaveFormat.Docx, watermarkImage, options);
```

### أنظر أيضا

* class [Watermarker](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)

---

## SetImage(*string, string, string, [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)*) {#setimage_7}

يضيف علامة مائية للصورة إلى المستند باستخدام الخيارات.

```csharp
public static void SetImage(string inputFileName, string outputFileName, 
    string watermarkImageFileName, ImageWatermarkOptions options)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| inputFileName | String | اسم ملف الإدخال. |
| outputFileName | String | اسم ملف الإخراج. |
| watermarkImageFileName | String | صورة يتم عرضها كعلامة مائية. |
| options | ImageWatermarkOptions | يحدد خيارات إضافية للعلامة المائية للصورة. |

## ملاحظات

إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، فسيتم حفظ كل صفحة من الإخراج كملف منفصل. سيتم استخدام اسم ملف الإخراج المحدد لإنشاء أسماء ملفات لكل جزء وفقًا للقاعدة: outputFile_partIndex.extension.

إذا كان تنسيق الإخراج هو TIFF، فسيتم حفظ الإخراج كملف TIFF متعدد الإطارات.

## أمثلة

يوضح كيفية إدراج صورة العلامة المائية في المستند.

```csharp
string doc = MyDir + "Document.docx";
string watermarkImage = ImageDir + "Logo.jpg";

Watermarker.SetImage(doc, ArtifactsDir + "LowCode.SetWatermarkImage.1.docx", watermarkImage);
Watermarker.SetImage(doc, ArtifactsDir + "LowCode.SetWatermarkText.2.docx", SaveFormat.Docx, watermarkImage);

ImageWatermarkOptions options = new ImageWatermarkOptions();
options.Scale = 50;
Watermarker.SetImage(doc, ArtifactsDir + "LowCode.SetWatermarkText.3.docx", watermarkImage, options);
Watermarker.SetImage(doc, ArtifactsDir + "LowCode.SetWatermarkText.4.docx", SaveFormat.Docx, watermarkImage, options);
```

### أنظر أيضا

* class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* class [Watermarker](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)

---

## SetImage(*string, string, [SaveFormat](../../../aspose.words/saveformat/), string, [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)*) {#setimage_4}

يضيف علامة مائية للصورة إلى المستند مع خيارات وتنسيق حفظ محدد.

```csharp
public static void SetImage(string inputFileName, string outputFileName, SaveFormat saveFormat, 
    string watermarkImageFileName, ImageWatermarkOptions options = null)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| inputFileName | String | اسم ملف الإدخال. |
| outputFileName | String | اسم ملف الإخراج. |
| saveFormat | SaveFormat | تنسيق الحفظ. |
| watermarkImageFileName | String | صورة يتم عرضها كعلامة مائية. |
| options | ImageWatermarkOptions | يحدد خيارات إضافية للعلامة المائية للصورة. |

## ملاحظات

إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، فسيتم حفظ كل صفحة من الإخراج كملف منفصل. سيتم استخدام اسم ملف الإخراج المحدد لإنشاء أسماء ملفات لكل جزء وفقًا للقاعدة: outputFile_partIndex.extension.

إذا كان تنسيق الإخراج هو TIFF، فسيتم حفظ الإخراج كملف TIFF متعدد الإطارات.

## أمثلة

يوضح كيفية إدراج صورة العلامة المائية في المستند.

```csharp
string doc = MyDir + "Document.docx";
string watermarkImage = ImageDir + "Logo.jpg";

Watermarker.SetImage(doc, ArtifactsDir + "LowCode.SetWatermarkImage.1.docx", watermarkImage);
Watermarker.SetImage(doc, ArtifactsDir + "LowCode.SetWatermarkText.2.docx", SaveFormat.Docx, watermarkImage);

ImageWatermarkOptions options = new ImageWatermarkOptions();
options.Scale = 50;
Watermarker.SetImage(doc, ArtifactsDir + "LowCode.SetWatermarkText.3.docx", watermarkImage, options);
Watermarker.SetImage(doc, ArtifactsDir + "LowCode.SetWatermarkText.4.docx", SaveFormat.Docx, watermarkImage, options);
```

### أنظر أيضا

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* class [Watermarker](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)

---

## SetImage(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), string, [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)*) {#setimage_5}

يضيف علامة مائية للصورة إلى المستند مع خيارات وتنسيق حفظ محدد.

```csharp
public static void SetImage(string inputFileName, string outputFileName, SaveOptions saveOptions, 
    string watermarkImageFileName, ImageWatermarkOptions options = null)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| inputFileName | String | اسم ملف الإدخال. |
| outputFileName | String | اسم ملف الإخراج. |
| saveOptions | SaveOptions | خيارات الحفظ. |
| watermarkImageFileName | String | صورة يتم عرضها كعلامة مائية. |
| options | ImageWatermarkOptions | يحدد خيارات إضافية للعلامة المائية للصورة. |

## ملاحظات

إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، فسيتم حفظ كل صفحة من الإخراج كملف منفصل. سيتم استخدام اسم ملف الإخراج المحدد لإنشاء أسماء ملفات لكل جزء وفقًا للقاعدة: outputFile_partIndex.extension.

إذا كان تنسيق الإخراج هو TIFF، فسيتم حفظ الإخراج كملف TIFF متعدد الإطارات.

### أنظر أيضا

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* class [Watermarker](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)

---

## SetImage(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), Image, [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)*) {#setimage}

يضيف علامة مائية للصورة إلى المستند من التدفقات التي تحتوي على خيارات.

```csharp
public static void SetImage(Stream inputStream, Stream outputStream, SaveFormat saveFormat, 
    Image watermarkImage, ImageWatermarkOptions options = null)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| inputStream | Stream | مجرى الإدخال. |
| outputStream | Stream | تيار الإخراج. |
| saveFormat | SaveFormat | تنسيق الحفظ. |
| watermarkImage | Image | صورة يتم عرضها كعلامة مائية. |
| options | ImageWatermarkOptions | يحدد خيارات إضافية للعلامة المائية للصورة. |

## ملاحظات

إذا كان تنسيق الإخراج عبارة عن صورة (BMP، أو EMF، أو EPS، أو GIF، أو JPEG، أو PNG، أو WebP)، فسيتم حفظ الصفحة الأولى فقط من الإخراج في التدفق المحدد.

إذا كان تنسيق الإخراج هو TIFF، فسيتم حفظ الإخراج كملف TIFF متعدد الإطارات إلى الدفق المحدد.

## أمثلة

يوضح كيفية إدراج صورة العلامة المائية في المستند من مجرى مائي.

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.SetWatermarkText.1.docx", FileMode.Create, FileAccess.ReadWrite))
        Watermarker.SetImage(streamIn, streamOut, SaveFormat.Docx, System.Drawing.Image.FromFile(ImageDir + "Logo.jpg"));
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.SetWatermarkText.2.docx", FileMode.Create, FileAccess.ReadWrite))
        Watermarker.SetImage(streamIn, streamOut, SaveFormat.Docx, System.Drawing.Image.FromFile(ImageDir + "Logo.jpg"), new ImageWatermarkOptions() { Scale = 50 });
}
```

### أنظر أيضا

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* class [Watermarker](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)

---

## SetImage(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), Image, [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)*) {#setimage_2}

يضيف علامة مائية للصورة إلى المستند من التدفقات التي تحتوي على خيارات.

```csharp
public static void SetImage(Stream inputStream, Stream outputStream, SaveOptions saveOptions, 
    Image watermarkImage, ImageWatermarkOptions options = null)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| inputStream | Stream | مجرى الإدخال. |
| outputStream | Stream | تيار الإخراج. |
| saveOptions | SaveOptions | خيارات الحفظ. |
| watermarkImage | Image | صورة يتم عرضها كعلامة مائية. |
| options | ImageWatermarkOptions | يحدد خيارات إضافية للعلامة المائية للصورة. |

## ملاحظات

إذا كان تنسيق الإخراج عبارة عن صورة (BMP، أو EMF، أو EPS، أو GIF، أو JPEG، أو PNG، أو WebP)، فسيتم حفظ الصفحة الأولى فقط من الإخراج في التدفق المحدد.

إذا كان تنسيق الإخراج هو TIFF، فسيتم حفظ الإخراج كملف TIFF متعدد الإطارات إلى الدفق المحدد.

### أنظر أيضا

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* class [Watermarker](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)

---

## SetImage(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), Stream, [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)*) {#setimage_1}

يضيف علامة مائية للصورة إلى المستند من التدفقات التي تحتوي على خيارات.

```csharp
public static void SetImage(Stream inputStream, Stream outputStream, SaveFormat saveFormat, 
    Stream watermarkImageStream, ImageWatermarkOptions options = null)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| inputStream | Stream | مجرى الإدخال. |
| outputStream | Stream | تيار الإخراج. |
| saveFormat | SaveFormat | تنسيق الحفظ. |
| watermarkImageStream | Stream | تدفق الصورة الذي يتم عرضه كعلامة مائية. |
| options | ImageWatermarkOptions | يحدد خيارات إضافية للعلامة المائية للصورة. |

## ملاحظات

إذا كان تنسيق الإخراج عبارة عن صورة (BMP، أو EMF، أو EPS، أو GIF، أو JPEG، أو PNG، أو WebP)، فسيتم حفظ الصفحة الأولى فقط من الإخراج في التدفق المحدد.

إذا كان تنسيق الإخراج هو TIFF، فسيتم حفظ الإخراج كملف TIFF متعدد الإطارات إلى الدفق المحدد.

### أنظر أيضا

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* class [Watermarker](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)

---

## SetImage(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), Stream, [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)*) {#setimage_3}

يضيف علامة مائية للصورة إلى المستند من التدفقات التي تحتوي على خيارات.

```csharp
public static void SetImage(Stream inputStream, Stream outputStream, SaveOptions saveOptions, 
    Stream watermarkImageStream, ImageWatermarkOptions options = null)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| inputStream | Stream | مجرى الإدخال. |
| outputStream | Stream | تيار الإخراج. |
| saveOptions | SaveOptions | خيارات الحفظ. |
| watermarkImageStream | Stream | تدفق الصورة الذي يتم عرضه كعلامة مائية. |
| options | ImageWatermarkOptions | يحدد خيارات إضافية للعلامة المائية للصورة. |

## ملاحظات

إذا كان تنسيق الإخراج عبارة عن صورة (BMP، أو EMF، أو EPS، أو GIF، أو JPEG، أو PNG، أو WebP)، فسيتم حفظ الصفحة الأولى فقط من الإخراج في التدفق المحدد.

إذا كان تنسيق الإخراج هو TIFF، فسيتم حفظ الإخراج كملف TIFF متعدد الإطارات إلى الدفق المحدد.

### أنظر أيضا

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* class [Watermarker](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)
