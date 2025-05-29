---
title: ShapeBase.AspectRatioLocked
linktitle: AspectRatioLocked
articleTitle: AspectRatioLocked
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ShapeBase AspectRatioLocked للحفاظ على نسبة أبعاد أشكالك بسهولة للحصول على تصاميم مثالية. حسّن مشاريعك اليوم!
type: docs
weight: 40
url: /ar/net/aspose.words.drawing/shapebase/aspectratiolocked/
---
## ShapeBase.AspectRatioLocked property

يحدد ما إذا كانت نسبة العرض إلى الارتفاع للشكل مقفلة.

```csharp
public bool AspectRatioLocked { get; set; }
```

## ملاحظات

القيمة الافتراضية تعتمد على[`ShapeType`](../../shapetype/) ، من أجلImage إنها`حقيقي` ولكن بالنسبة لأنواع الأشكال الأخرى فهي`خطأ شنيع`.

ينطبق التأثير على الأشكال ذات المستوى الأعلى فقط.

## أمثلة

يوضح كيفية قفل/فتح نسبة العرض إلى الارتفاع للشكل.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// إدراج شكل. إذا فتحنا هذا المستند في مايكروسوفت وورد، يمكننا النقر بزر الماوس الأيمن على الشكل لإظهاره.
// ثمانية مقابض تغيير الحجم حول محيطها، والتي يمكننا النقر عليها وسحبها لتغيير حجمها.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");

// اضبط خاصية "AspectRatioLocked" على "true" للحفاظ على نسبة العرض إلى الارتفاع للشكل
// عند استخدام أي من مقابض تغيير الحجم القطرية الأربعة، والتي تعمل على تغيير كل من ارتفاع الصورة وعرضها.
// سيؤدي استخدام أي مقابض تغيير الحجم المتعامدة التي تغير الارتفاع أو العرض إلى تغيير نسبة العرض إلى الارتفاع.
// اضبط خاصية "AspectRatioLocked" على "false" للسماح لنا بـ
// قم بتغيير نسبة العرض إلى الارتفاع للصورة بحرية باستخدام كافة مقابض تغيير الحجم.
shape.AspectRatioLocked = lockAspectRatio;

doc.Save(ArtifactsDir + "Shape.AspectRatio.docx");
```

### أنظر أيضا

* class [ShapeBase](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
