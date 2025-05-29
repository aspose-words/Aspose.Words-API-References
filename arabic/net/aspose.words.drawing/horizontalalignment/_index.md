---
title: HorizontalAlignment Enum
linktitle: HorizontalAlignment
articleTitle: HorizontalAlignment
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Aspose.Words.Drawing.HorizontalAlignment للتحكم الدقيق في المحاذاة الأفقية في إطارات النصوص العائمة والجداول. حسّن تصميم مستندك!
type: docs
weight: 1360
url: /ar/net/aspose.words.drawing/horizontalalignment/
---
## HorizontalAlignment enumeration

يحدد المحاذاة الأفقية لشكل عائم أو إطار نص أو جدول عائم.

```csharp
public enum HorizontalAlignment
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| None | `0` | يتم وضع الكائن بشكل صريح، عادةً باستخدام**غادر** الملكية. |
| Default | `0` | نفس الشيءNone . |
| Left | `1` | يحدد أن الكائن يجب أن يكون محاذيًا لليسار مع قاعدة المحاذاة الأفقية. |
| Center | `2` | يحدد أن الكائن يجب أن يكون متمركزًا بالنسبة لقاعدة المحاذاة الأفقية. |
| Right | `3` | يحدد أن الكائن يجب أن يكون محاذيًا لليمين مع قاعدة المحاذاة الأفقية. |
| Inside | `4` | يحدد أن الكائن يجب أن يكون داخل قاعدة المحاذاة الأفقية. |
| Outside | `5` | يحدد أن الكائن يجب أن يكون خارج قاعدة المحاذاة الأفقية. |

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

### أنظر أيضا

* property [HorizontalAlignment](../shapebase/horizontalalignment/)
* مساحة الاسم [Aspose.Words.Drawing](../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../)
