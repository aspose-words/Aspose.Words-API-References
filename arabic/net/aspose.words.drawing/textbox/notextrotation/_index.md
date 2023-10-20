---
title: TextBox.NoTextRotation
linktitle: NoTextRotation
articleTitle: NoTextRotation
second_title: Aspose.Words لـ .NET
description: TextBox NoTextRotation ملكية. الحصول على قيمة منطقية أو تعيينها تشير إلى عدم تدوير نص مربع النص عند تدوير الشكل في C#.
type: docs
weight: 80
url: /ar/net/aspose.words.drawing/textbox/notextrotation/
---
## TextBox.NoTextRotation property

الحصول على قيمة منطقية أو تعيينها تشير إلى عدم تدوير نص مربع النص عند تدوير الشكل.

```csharp
public bool NoTextRotation { get; set; }
```

## ملاحظات

القيمة الافتراضية هي`خطأ شنيع`

## أمثلة

يوضح كيفية تعطيل تدوير النص عند تدوير الشكل.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Ellipse, 20, 20);
shape.TextBox.NoTextRotation = true;

doc.Save(ArtifactsDir + "Shape.NoTextRotation.docx");
```

### أنظر أيضا

* class [TextBox](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
