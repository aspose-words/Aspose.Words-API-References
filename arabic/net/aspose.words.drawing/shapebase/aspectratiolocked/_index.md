---
title: ShapeBase.AspectRatioLocked
second_title: Aspose.Words لمراجع .NET API
description: ShapeBase ملكية. يحدد ما إذا كانت نسبة العرض إلى الارتفاع للشكل مؤمنة.
type: docs
weight: 40
url: /ar/net/aspose.words.drawing/shapebase/aspectratiolocked/
---
## ShapeBase.AspectRatioLocked property

يحدد ما إذا كانت نسبة العرض إلى الارتفاع للشكل مؤمنة.

```csharp
public bool AspectRatioLocked { get; set; }
```

### ملاحظات

تعتمد القيمة الافتراضية على[`ShapeType`](../shapetype/) ، من أجل ShapeType. الصورة هو **حقيقي** ولكن بالنسبة لأنواع الأشكال الأخرى فهو كذلك **خاطئة**.

له تأثير لأشكال المستوى الأعلى فقط.

### أمثلة

يوضح كيفية قفل / فتح نسبة العرض إلى الارتفاع للشكل.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل شكل. إذا فتحنا هذا المستند في Microsoft Word ، فيمكننا ترك النقر فوق الشكل للكشف عنه
// ثمانية مقابض تحجيم حول محيطها ، والتي يمكننا النقر عليها وسحبها لتغيير حجمها.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");

// اضبط خاصية "AspectRatioLocked" على "true" للحفاظ على نسبة العرض إلى الارتفاع للشكل
// عند استخدام أي من مقابض التحجيم القطرية الأربعة ، والتي تغير ارتفاع الصورة وعرضها.
// باستخدام أي مقابض تغيير حجم متعامدة إما أن تغير الارتفاع أو العرض ستظل تغير نسبة العرض إلى الارتفاع.
// اضبط خاصية "AspectRatioLocked" على "false" للسماح لنا بذلك
// تغيير نسبة أبعاد الصورة بحرية مع جميع مقابض التحجيم.
shape.AspectRatioLocked = lockAspectRatio;

doc.Save(ArtifactsDir + "Shape.AspectRatio.docx");
```

### أنظر أيضا

* class [ShapeBase](../)
* مساحة الاسم [Aspose.Words.Drawing](../../shapebase/)
* المجسم [Aspose.Words](../../../)


