---
title: TextureAlignment Enum
linktitle: TextureAlignment
articleTitle: TextureAlignment
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Drawing.TextureAlignment تعداد. يحدد المحاذاة لتبليط تعبئة النسيج في C#.
type: docs
weight: 1370
url: /ar/net/aspose.words.drawing/texturealignment/
---
## TextureAlignment enumeration

يحدد المحاذاة لتبليط تعبئة النسيج.

```csharp
public enum TextureAlignment
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| TopLeft | `0` | محاذاة النسيج العلوي الأيسر. |
| Top | `1` | محاذاة النسيج العلوي. |
| TopRight | `2` | محاذاة النسيج العلوي الأيمن. |
| Left | `3` | محاذاة المادة لليسار. |
| Center | `4` | محاذاة النسيج للمركز. |
| Right | `5` | محاذاة الملمس لليمين. |
| BottomLeft | `6` | محاذاة الملمس السفلي الأيسر. |
| Bottom | `7` | محاذاة النسيج السفلي. |
| BottomRight | `8` | محاذاة الملمس السفلي الأيمن. |
| None | `9` | لا توجد محاذاة للنسيج. |

## أمثلة

يوضح كيفية تعبئة وتبليط النسيج داخل الشكل.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);

// تطبيق محاذاة النسيج على تعبئة الشكل.
shape.Fill.PresetTextured(PresetTexture.Canvas);
shape.Fill.TextureAlignment = TextureAlignment.TopRight;

// استخدم خيار الامتثال لتحديد الشكل باستخدام DML إذا كنت تريد الحصول على "TextureAlignment"
// الخاصية بعد حفظ المستند.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Compliance = OoxmlCompliance.Iso29500_2008_Strict };

doc.Save(ArtifactsDir + "Shape.TextureFill.docx", saveOptions);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Drawing](../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../)
