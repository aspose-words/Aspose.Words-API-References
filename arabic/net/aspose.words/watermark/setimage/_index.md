---
title: Watermark.SetImage
linktitle: SetImage
articleTitle: SetImage
second_title: Aspose.Words لـ .NET
description: أضف علامات مائية رائعة لصورك بكل سهولة لإضفاء لمسة احترافية على مستنداتك باستخدام طريقة Watermark SetImage.
type: docs
weight: 30
url: /ar/net/aspose.words/watermark/setimage/
---
## SetImage(*Image*) {#setimage}

يضيف علامة مائية للصورة إلى المستند.

```csharp
public void SetImage(Image image)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| image | Image | صورة يتم عرضها كعلامة مائية. |

### استثناءات

| استثناء | حالة |
| --- | --- |
| ArgumentNullException | يتم طرحه عندما تكون الصورة`باطل` . |

## أمثلة

يوضح كيفية إنشاء علامة مائية من صورة في نظام الملفات المحلي.

```csharp
Document doc = new Document();

            // تعديل مظهر العلامة المائية للصورة باستخدام كائن ImageWatermarkOptions،
            // ثم مررها أثناء إنشاء علامة مائية من ملف صورة.
            ImageWatermarkOptions imageWatermarkOptions = new ImageWatermarkOptions();
            imageWatermarkOptions.Scale = 5;
            imageWatermarkOptions.IsWashout = false;

#if NET461_OR_GREATER || JAVA
            // لدينا خيارات مختلفة لإدراج الصورة:
            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"), imageWatermarkOptions);

            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"));

            doc.Watermark.SetImage(ImageDir + "Logo.jpg", imageWatermarkOptions);
#elif NET5_0_OR_GREATER
            using (SKBitmap image = SKBitmap.Decode(ImageDir + "Logo.jpg"))
            {
                doc.Watermark.SetImage(image, imageWatermarkOptions);
            }
#endif

            doc.Save(ArtifactsDir + "Document.ImageWatermark.docx");
```

### أنظر أيضا

* class [Watermark](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## SetImage(*Image, [ImageWatermarkOptions](../../imagewatermarkoptions/)*) {#setimage_1}

يضيف علامة مائية للصورة إلى المستند.

```csharp
public void SetImage(Image image, ImageWatermarkOptions options)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| image | Image | صورة يتم عرضها كعلامة مائية. |
| options | ImageWatermarkOptions | يحدد خيارات إضافية للعلامة المائية للصورة. |

### استثناءات

| استثناء | حالة |
| --- | --- |
| ArgumentNullException | يتم طرحه عندما تكون الصورة`باطل` . |

## ملاحظات

لو[`ImageWatermarkOptions`](../../imagewatermarkoptions/) يكون`باطل`سيتم تعيين العلامة المائية بالخيارات الافتراضية.

## أمثلة

يوضح كيفية إنشاء علامة مائية من صورة في نظام الملفات المحلي.

```csharp
Document doc = new Document();

            // تعديل مظهر العلامة المائية للصورة باستخدام كائن ImageWatermarkOptions،
            // ثم مررها أثناء إنشاء علامة مائية من ملف صورة.
            ImageWatermarkOptions imageWatermarkOptions = new ImageWatermarkOptions();
            imageWatermarkOptions.Scale = 5;
            imageWatermarkOptions.IsWashout = false;

#if NET461_OR_GREATER || JAVA
            // لدينا خيارات مختلفة لإدراج الصورة:
            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"), imageWatermarkOptions);

            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"));

            doc.Watermark.SetImage(ImageDir + "Logo.jpg", imageWatermarkOptions);
#elif NET5_0_OR_GREATER
            using (SKBitmap image = SKBitmap.Decode(ImageDir + "Logo.jpg"))
            {
                doc.Watermark.SetImage(image, imageWatermarkOptions);
            }
#endif

            doc.Save(ArtifactsDir + "Document.ImageWatermark.docx");
```

### أنظر أيضا

* class [ImageWatermarkOptions](../../imagewatermarkoptions/)
* class [Watermark](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## SetImage(*string, [ImageWatermarkOptions](../../imagewatermarkoptions/)*) {#setimage_3}

يضيف علامة مائية للصورة إلى المستند.

```csharp
public void SetImage(string imagePath, ImageWatermarkOptions options)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| imagePath | String | المسار إلى ملف الصورة الذي يتم عرضه كعلامة مائية. |
| options | ImageWatermarkOptions | يحدد خيارات إضافية للعلامة المائية للصورة. |

### استثناءات

| استثناء | حالة |
| --- | --- |
| ArgumentNullException | يتم طرحه عندما يكون المسار`باطل` . |

## ملاحظات

لو[`ImageWatermarkOptions`](../../imagewatermarkoptions/) يكون`باطل`سيتم تعيين العلامة المائية بالخيارات الافتراضية.

## أمثلة

يوضح كيفية إنشاء علامة مائية من صورة في نظام الملفات المحلي.

```csharp
Document doc = new Document();

            // تعديل مظهر العلامة المائية للصورة باستخدام كائن ImageWatermarkOptions،
            // ثم مررها أثناء إنشاء علامة مائية من ملف صورة.
            ImageWatermarkOptions imageWatermarkOptions = new ImageWatermarkOptions();
            imageWatermarkOptions.Scale = 5;
            imageWatermarkOptions.IsWashout = false;

#if NET461_OR_GREATER || JAVA
            // لدينا خيارات مختلفة لإدراج الصورة:
            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"), imageWatermarkOptions);

            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"));

            doc.Watermark.SetImage(ImageDir + "Logo.jpg", imageWatermarkOptions);
#elif NET5_0_OR_GREATER
            using (SKBitmap image = SKBitmap.Decode(ImageDir + "Logo.jpg"))
            {
                doc.Watermark.SetImage(image, imageWatermarkOptions);
            }
#endif

            doc.Save(ArtifactsDir + "Document.ImageWatermark.docx");
```

### أنظر أيضا

* class [ImageWatermarkOptions](../../imagewatermarkoptions/)
* class [Watermark](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## SetImage(*Stream, [ImageWatermarkOptions](../../imagewatermarkoptions/)*) {#setimage_2}

يضيف علامة مائية للصورة إلى المستند.

```csharp
public void SetImage(Stream imageStream, ImageWatermarkOptions options)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| imageStream | Stream | التدفق الذي يحتوي على بيانات الصورة التي يتم عرضها كعلامة مائية. |
| options | ImageWatermarkOptions | يحدد خيارات إضافية للعلامة المائية للصورة. |

### استثناءات

| استثناء | حالة |
| --- | --- |
| ArgumentNullException | يتم طرحه عندما يكون المسار`باطل` . |

## ملاحظات

لو[`ImageWatermarkOptions`](../../imagewatermarkoptions/) يكون`باطل`سيتم تعيين العلامة المائية بالخيارات الافتراضية.

## أمثلة

يوضح كيفية إنشاء علامة مائية من مجرى صورة.

```csharp
Document doc = new Document();

// تعديل مظهر العلامة المائية للصورة باستخدام كائن ImageWatermarkOptions،
// ثم مررها أثناء إنشاء علامة مائية من ملف صورة.
ImageWatermarkOptions imageWatermarkOptions = new ImageWatermarkOptions();
imageWatermarkOptions.Scale = 5;

using (FileStream imageStream = new FileStream(ImageDir + "Logo.jpg", FileMode.Open, FileAccess.Read))
    doc.Watermark.SetImage(imageStream, imageWatermarkOptions);

doc.Save(ArtifactsDir + "Document.ImageWatermarkStream.docx");
```

### أنظر أيضا

* class [ImageWatermarkOptions](../../imagewatermarkoptions/)
* class [Watermark](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
