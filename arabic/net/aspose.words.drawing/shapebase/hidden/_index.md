---
title: ShapeBase.Hidden
linktitle: Hidden
articleTitle: Hidden
second_title: Aspose.Words لـ .NET
description: تحكم في رؤية الشكل باستخدام خاصية إخفاء ShapeBase. يمكنك التبديل بسهولة بين الإخفاء والظهور لمرونة تصميم أكبر.
type: docs
weight: 230
url: /ar/net/aspose.words.drawing/shapebase/hidden/
---
## ShapeBase.Hidden property

يحصل على قيمة منطقية أو يعينها للإشارة إلى ما إذا كان الشكل مرئيًا أم لا.

```csharp
public bool Hidden { get; set; }
```

## ملاحظات

القيمة الافتراضية هي`خطأ شنيع` .

## أمثلة

يوضح كيفية إخفاء الشكل.

```csharp
Document doc = new Document(MyDir + "Shadow color.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
if (!shape.Hidden)
    shape.Hidden = true;

doc.Save(ArtifactsDir + "Shape.Hidden.docx");
```

### أنظر أيضا

* class [ShapeBase](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
