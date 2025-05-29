---
title: ImageColorMode Enum
linktitle: ImageColorMode
articleTitle: ImageColorMode
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Aspose.Words.Saving.ImageColorMode لتحسين صور صفحات المستندات. تحكم في أوضاع الألوان لتحسين جودة الصور في مشاريعك.
type: docs
weight: 5960
url: /ar/net/aspose.words.saving/imagecolormode/
---
## ImageColorMode enumeration

يحدد وضع اللون للصور المولدة لصفحات المستند.

```csharp
public enum ImageColorMode
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| None | `0` | سيتم عرض صفحات المستند كصور ملونة. |
| Grayscale | `1` | سيتم عرض صفحات المستند كصور بدرجات الرمادي. |
| BlackAndWhite | `2` | سيتم عرض صفحات المستند كصور بالأبيض والأسود. |

## أمثلة

يوضح كيفية تعيين وضع الألوان عند عرض المستندات.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// عندما نحفظ المستند كصورة، يمكننا تمرير كائن SaveOptions إلى
// حدد وضع اللون للصورة التي سيتم إنشاءها من خلال عملية الحفظ.
// إذا قمنا بتعيين خاصية "ImageColorMode" إلى "ImageColorMode.BlackAndWhite"،
// ستطبق عملية الحفظ تقليل لون التدرج الرمادي أثناء عرض المستند.
 // إذا قمنا بتعيين خاصية "ImageColorMode" إلى "ImageColorMode.Grayscale"،
// ستؤدي عملية الحفظ إلى تحويل المستند إلى صورة أحادية اللون.
// إذا قمنا بتعيين خاصية "ImageColorMode" إلى "None"، فسوف تطبق عملية الحفظ الطريقة الافتراضية
// والحفاظ على كافة ألوان المستند في الصورة الناتجة.
ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
imageSaveOptions.ImageColorMode = imageColorMode;

doc.Save(ArtifactsDir + "ImageSaveOptions.ColorMode.png", imageSaveOptions);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)
