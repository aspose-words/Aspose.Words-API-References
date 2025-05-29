---
title: WrapType Enum
linktitle: WrapType
articleTitle: WrapType
second_title: Aspose.Words لـ .NET
description: اكتشف كيف يعمل Aspose.Words.Drawing.WrapType على تعزيز التفاف النص حول الأشكال والصور لتنسيق المستندات بشكل احترافي.
type: docs
weight: 1810
url: /ar/net/aspose.words.drawing/wraptype/
---
## WrapType enumeration

يحدد كيفية لف النص حول الشكل أو الصورة.

```csharp
public enum WrapType
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| None | `3` | لا يوجد نص يلتف حول الشكل. الشكل موضوع خلف النص أو أمامه. |
| Inline | `0` | يبقى الشكل على نفس الطبقة مثل النص ويتم التعامل معه كحرف. |
| TopBottom | `1` | يتوقف النص في أعلى الشكل ويبدأ من جديد على السطر الموجود أسفل الشكل. |
| Square | `2` | يلتف النص حول جميع جوانب المربع المحيط بالشكل. |
| Tight | `4` | يلتف بشكل محكم حول حواف الشكل، بدلاً من الالتفاف حول المربع المحدد. |
| Through | `5` | نفس الشيء مثل Tight، لكنه يلتف داخل أي أجزاء من الشكل مفتوحة. |

## أمثلة

يوضح كيفية إدراج صورة عائمة في وسط الصفحة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بإدراج صورة عائمة ستظهر خلف النص المتداخل وقم بمحاذاتها مع مركز الصفحة.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;
shape.BehindText = true;
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.HorizontalAlignment = HorizontalAlignment.Center;
shape.VerticalAlignment = VerticalAlignment.Center;

doc.Save(ArtifactsDir + "Image.CreateFloatingPageCenter.docx");
```

يوضح كيفية إدراج صورة واستخدامها كعلامة مائية.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

//أدرج الصورة في الرأس حتى تكون مرئية في كل صفحة.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
Shape shape = builder.InsertImage(ImageDir + "Transparent background logo.png");
shape.WrapType = WrapType.None;
shape.BehindText = true;

// ضع الصورة في وسط الصفحة.
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.Left = (builder.PageSetup.PageWidth - shape.Width) / 2;
shape.Top = (builder.PageSetup.PageHeight - shape.Height) / 2;

doc.Save(ArtifactsDir + "DocumentBuilder.InsertWatermark.docx");
```

### أنظر أيضا

* property [WrapType](../shapebase/wraptype/)
* مساحة الاسم [Aspose.Words.Drawing](../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../)
