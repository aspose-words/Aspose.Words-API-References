---
title: Watermarker.SetWatermarkToImages
linktitle: SetWatermarkToImages
articleTitle: SetWatermarkToImages
second_title: Aspose.Words لـ .NET
description: قم بتعزيز صورك باستخدام طريقة Watermarker Set الخاصة بنا، من خلال إضافة علامات مائية نصية قابلة للتخصيص للحصول على لمسة احترافية وإخراج سلس.
type: docs
weight: 40
url: /ar/net/aspose.words.lowcode/watermarker/setwatermarktoimages/
---
## SetWatermarkToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), string, [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)*) {#setwatermarktoimages_3}

يُضيف علامة مائية نصية إلى المستند مع خيارات. يُحوّل المخرجات إلى صور.

```csharp
public static Stream[] SetWatermarkToImages(string inputFileName, ImageSaveOptions saveOptions, 
    string watermarkText, TextWatermarkOptions options = null)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| inputFileName | String | اسم ملف الإدخال. |
| saveOptions | ImageSaveOptions | خيارات الحفظ. |
| watermarkText | String | النص الذي يتم عرضه كعلامة مائية. |
| options | TextWatermarkOptions | يحدد خيارات إضافية للعلامة المائية النصية. |

## أمثلة

يوضح كيفية إدراج نص العلامة المائية في المستند وحفظ النتيجة في الصور.

```csharp
string doc = MyDir + "Big document.docx";
string watermarkText = "This is a watermark";

Stream[] images = Watermarker.SetWatermarkToImages(doc, new ImageSaveOptions(SaveFormat.Png), watermarkText);

TextWatermarkOptions watermarkOptions = new TextWatermarkOptions();
watermarkOptions.Color = Color.Red;
images = Watermarker.SetWatermarkToImages(doc, new ImageSaveOptions(SaveFormat.Png), watermarkText, watermarkOptions);
```

### أنظر أيضا

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* class [Watermarker](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)

---

## SetWatermarkToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), string, [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)*) {#setwatermarktoimages_1}

يُضيف علامة مائية نصية إلى المستند مع خيارات. يُحوّل المخرجات إلى صور.

```csharp
public static Stream[] SetWatermarkToImages(Stream inputStream, ImageSaveOptions saveOptions, 
    string watermarkText, TextWatermarkOptions options = null)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| inputStream | Stream | تدفق ملف الإدخال. |
| saveOptions | ImageSaveOptions | خيارات الحفظ. |
| watermarkText | String | النص الذي يتم عرضه كعلامة مائية. |
| options | TextWatermarkOptions | يحدد خيارات إضافية للعلامة المائية النصية. |

## أمثلة

يوضح كيفية إدراج نص العلامة المائية في المستند من الدفق وحفظ النتيجة في الصور.

```csharp
string watermarkText = "This is a watermark";

using (FileStream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open, FileAccess.Read))
{
    Stream[] images = Watermarker.SetWatermarkToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), watermarkText);

    TextWatermarkOptions watermarkOptions = new TextWatermarkOptions();
    watermarkOptions.Color = Color.Red;
    images = Watermarker.SetWatermarkToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), watermarkText, watermarkOptions);
}
```

### أنظر أيضا

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* class [Watermarker](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)

---

## SetWatermarkToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), byte[], [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)*) {#setwatermarktoimages_2}

يُضيف علامة مائية للصورة إلى المستند مع خيارات. يُحوّل المخرجات إلى صور.

```csharp
public static Stream[] SetWatermarkToImages(string inputFileName, ImageSaveOptions saveOptions, 
    byte[] watermarkImageBytes, ImageWatermarkOptions options = null)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| inputFileName | String | اسم ملف الإدخال. |
| saveOptions | ImageSaveOptions | خيارات الحفظ. |
| watermarkImageBytes | Byte[] | بايتات الصورة التي يتم عرضها كعلامة مائية. |
| options | ImageWatermarkOptions | يحدد خيارات إضافية للعلامة المائية للصورة. |

## أمثلة

يوضح كيفية إدراج صورة العلامة المائية في المستند وحفظ النتيجة في الصور.

```csharp
string doc = MyDir + "Document.docx";
string watermarkImage = ImageDir + "Logo.jpg";

Watermarker.SetWatermarkToImages(doc, new ImageSaveOptions(SaveFormat.Png), File.ReadAllBytes(watermarkImage));

ImageWatermarkOptions options = new ImageWatermarkOptions();
options.Scale = 50;
Watermarker.SetWatermarkToImages(doc, new ImageSaveOptions(SaveFormat.Png), File.ReadAllBytes(watermarkImage), options);
```

### أنظر أيضا

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* class [Watermarker](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)

---

## SetWatermarkToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), Stream, [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)*) {#setwatermarktoimages}

يُضيف علامة مائية للصورة إلى المستند مع خيارات. يُحوّل المخرجات إلى صور.

```csharp
public static Stream[] SetWatermarkToImages(Stream inputStream, ImageSaveOptions saveOptions, 
    Stream watermarkImageStream, ImageWatermarkOptions options = null)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| inputStream | Stream | مجرى الإدخال. |
| saveOptions | ImageSaveOptions | خيارات الحفظ. |
| watermarkImageStream | Stream | تدفق الصورة الذي يتم عرضه كعلامة مائية. |
| options | ImageWatermarkOptions | يحدد خيارات إضافية للعلامة المائية للصورة. |

## أمثلة

يوضح كيفية إدراج صورة العلامة المائية في المستند من مجرى وحفظ النتيجة في الصور.

```csharp
string watermarkImage = ImageDir + "Logo.jpg";

using (FileStream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream imageStream = new FileStream(watermarkImage, FileMode.Open, FileAccess.Read))
    {
        Watermarker.SetWatermarkToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), imageStream);
        Watermarker.SetWatermarkToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), imageStream, new ImageWatermarkOptions() { Scale = 50 });
    }
}
```

### أنظر أيضا

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* class [Watermarker](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)
