---
title: ShapeBase.AspectRatioLocked
linktitle: AspectRatioLocked
articleTitle: AspectRatioLocked
second_title: Aspose.Words لـ .NET
description: ShapeBase AspectRatioLocked ملكية. يحدد ما إذا كانت نسبة العرض إلى الارتفاع للشكل مقفلة أم لا في C#.
type: docs
weight: 40
url: /ar/net/aspose.words.drawing/shapebase/aspectratiolocked/
---
## ShapeBase.AspectRatioLocked property

يحدد ما إذا كانت نسبة العرض إلى الارتفاع للشكل مقفلة أم لا.

```csharp
public bool AspectRatioLocked { get; set; }
```

## ملاحظات

القيمة الافتراضية تعتمد على[`ShapeType`](../../shapetype/) ، لImage إنها`حقيقي` ولكن بالنسبة لأنواع الأشكال الأخرى فهو كذلك`خطأ شنيع`.

له تأثير على أشكال المستوى الأعلى فقط.

## أمثلة

يوضح كيفية قفل/إلغاء قفل نسبة العرض إلى الارتفاع للشكل.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل شكلاً. إذا فتحنا هذا المستند في Microsoft Word، فيمكننا النقر بزر الماوس الأيسر على الشكل للكشف عنه
// ثمانية مقابض تغيير الحجم حول محيطه، والتي يمكننا النقر عليها وسحبها لتغيير حجمه.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");

// اضبط خاصية "AspectRatioLocked" على "صحيح" للحفاظ على نسبة العرض إلى الارتفاع للشكل
// عند استخدام أي من مقابض التحجيم القطرية الأربعة، والتي تغير كلاً من ارتفاع الصورة وعرضها.
// سيؤدي استخدام أي مقابض تغيير حجم متعامدة لتغيير الارتفاع أو العرض إلى تغيير نسبة العرض إلى الارتفاع.
// اضبط خاصية "AspectRatioLocked" على "خطأ" للسماح لنا بذلك
// قم بتغيير نسبة العرض إلى الارتفاع للصورة بحرية مع جميع مقابض التحجيم.
shape.AspectRatioLocked = lockAspectRatio;

doc.Save(ArtifactsDir + "Shape.AspectRatio.docx");
```

### أنظر أيضا

* class [ShapeBase](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
