---
title: ShapeBase.IsDecorative
linktitle: IsDecorative
articleTitle: IsDecorative
second_title: Aspose.Words لـ .NET
description: اكتشف ShapeBase. أدر خصائص الزخرفة في مستنداتك بسهولة. حسّن المظهر البصري من خلال تحديد علامات لتصاميم أشكال فريدة.
type: docs
weight: 260
url: /ar/net/aspose.words.drawing/shapebase/isdecorative/
---
## ShapeBase.IsDecorative property

يحصل على العلم الذي يحدد ما إذا كان الشكل مزخرفًا في المستند أم لا.

```csharp
public bool IsDecorative { get; set; }
```

## ملاحظات

لاحظ أن الشكل ليس فارغًا[`AlternativeText`](../alternativetext/) لا يمكن أن تكون زخرفية.

## أمثلة

يوضح كيفية ضبط الشكل ليكون زخرفيًا.

```csharp
Document doc = new Document(MyDir + "Decorative shapes.docx");

Shape shape = (Shape)doc.GetChildNodes(NodeType.Shape, true)[0];
Assert.True(shape.IsDecorative);

// إذا لم يكن "AlternativeText" فارغًا، فلا يمكن أن يكون الشكل زخرفيًا.
// لهذا السبب تغيرت قيمتنا إلى 'خطأ'.
shape.AlternativeText = "Alternative text.";
Assert.False(shape.IsDecorative);

DocumentBuilder builder = new DocumentBuilder(doc);

builder.MoveToDocumentEnd();
// إنشاء شكل جديد كزخرفي.
shape = builder.InsertShape(ShapeType.Rectangle, 100, 100);
shape.IsDecorative = true;

doc.Save(ArtifactsDir + "Shape.IsDecorative.docx");
```

### أنظر أيضا

* class [ShapeBase](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
