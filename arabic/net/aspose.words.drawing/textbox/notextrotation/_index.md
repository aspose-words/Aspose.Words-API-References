---
title: TextBox.NoTextRotation
linktitle: NoTextRotation
articleTitle: NoTextRotation
second_title: Aspose.Words لـ .NET
description: تحكم في تدوير النص في مربع النص باستخدام خاصية NoTextRotation. تأكد من وضوح النص وقراءته حتى عند تدوير الأشكال. حسّن تصميمك!
type: docs
weight: 80
url: /ar/net/aspose.words.drawing/textbox/notextrotation/
---
## TextBox.NoTextRotation property

يحصل على قيمة منطقية أو يعينها تشير إلى أنه لا ينبغي تدوير نص مربع النص عند تدوير الشكل.

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
