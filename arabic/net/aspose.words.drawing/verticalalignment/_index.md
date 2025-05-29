---
title: VerticalAlignment Enum
linktitle: VerticalAlignment
articleTitle: VerticalAlignment
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Aspose.Words.Drawing.VerticalAlignment لمحاذاة دقيقة عموديًا لإطارات النصوص والجداول في مستنداتك. حسّن التحكم في التخطيط!
type: docs
weight: 1790
url: /ar/net/aspose.words.drawing/verticalalignment/
---
## VerticalAlignment enumeration

يحدد المحاذاة الرأسية لشكل عائم أو إطار نص أو جدول عائم.

```csharp
public enum VerticalAlignment
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| None | `0` | يتم وضع الكائن بشكل صريح، عادةً باستخدام**قمة** الملكية. |
| Top | `1` | يحدد أن الكائن يجب أن يكون في أعلى قاعدة المحاذاة الرأسية. |
| Center | `2` | يحدد أن الكائن يجب أن يكون متمركزًا بالنسبة لقاعدة المحاذاة الرأسية. |
| Bottom | `3` | يحدد أن الكائن يجب أن يكون في أسفل قاعدة المحاذاة الرأسية. |
| Inside | `4` | يحدد أن الكائن يجب أن يكون داخل قاعدة المحاذاة الأفقية. |
| Outside | `5` | يحدد أن الكائن يجب أن يكون خارج قاعدة المحاذاة الرأسية. |
| Inline | `-1` | غير موثّق. يبدو أنها قيمة محتملة للفقرات والجداول العائمة. |
| Default | `0` | نفس الشيءNone . |

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

* property [VerticalAlignment](../shapebase/verticalalignment/)
* مساحة الاسم [Aspose.Words.Drawing](../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../)
