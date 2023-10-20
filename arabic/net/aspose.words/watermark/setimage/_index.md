---
title: Watermark.SetImage
linktitle: SetImage
articleTitle: SetImage
second_title: Aspose.Words لـ .NET
description: Watermark SetImage طريقة. يضيف علامة مائية للصورة إلى المستند في C#.
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
| image | Image | الصورة التي يتم عرضها كعلامة مائية. |

### استثناءات

| استثناء | حالة |
| --- | --- |
| ArgumentNullException | يرمي عندما تكون الصورة`باطل` . |

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
| image | Image | الصورة التي يتم عرضها كعلامة مائية. |
| options | ImageWatermarkOptions | يحدد خيارات إضافية للعلامة المائية للصورة. |

### استثناءات

| استثناء | حالة |
| --- | --- |
| ArgumentNullException | يرمي عندما تكون الصورة`باطل` . |

## ملاحظات

لو[`ImageWatermarkOptions`](../../imagewatermarkoptions/) يكون`باطل`سيتم تعيين العلامة المائية بالخيارات الافتراضية.

## أمثلة

يوضح كيفية إنشاء علامة مائية من صورة في نظام الملفات المحلي.

```csharp
Document doc = new Document();

            // تعديل مظهر العلامة المائية للصورة باستخدام كائن ImageWatermarkOptions،
            // ثم قم بتمريرها أثناء إنشاء علامة مائية من ملف صورة.
            ImageWatermarkOptions imageWatermarkOptions = new ImageWatermarkOptions();
            imageWatermarkOptions.Scale = 5;
            imageWatermarkOptions.IsWashout = false;

#if NET48 || JAVA
            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"), imageWatermarkOptions);
#elif NET5_0_OR_GREATER || __MOBILE__
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

## SetImage(*string, [ImageWatermarkOptions](../../imagewatermarkoptions/)*) {#setimage_2}

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
| ArgumentNullException | يرمي عندما يكون المسار`باطل` . |

## ملاحظات

لو[`ImageWatermarkOptions`](../../imagewatermarkoptions/) يكون`باطل`سيتم تعيين العلامة المائية بالخيارات الافتراضية.

### أنظر أيضا

* class [ImageWatermarkOptions](../../imagewatermarkoptions/)
* class [Watermark](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
