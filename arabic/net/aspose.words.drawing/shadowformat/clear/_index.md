---
title: ShadowFormat.Clear
linktitle: Clear
articleTitle: Clear
second_title: Aspose.Words لـ .NET
description: أعد ضبط تنسيق الظلال بسهولة باستخدام طريقة مسح تنسيق الظلال. حسّن تصميمك بلوحة نظيفة اليوم!
type: docs
weight: 40
url: /ar/net/aspose.words.drawing/shadowformat/clear/
---
## ShadowFormat.Clear method

يمسح تنسيق الظل.

```csharp
public void Clear()
```

## أمثلة

يوضح كيفية العمل مع تنسيق الظل للشكل.

```csharp
Document doc = new Document(MyDir + "Shape stroke pattern border.docx");
Shape shape = (Shape)doc.GetChildNodes(NodeType.Shape, true)[0];

if (shape.ShadowFormat.Visible && shape.ShadowFormat.Type == ShadowType.Shadow2)
    shape.ShadowFormat.Type = ShadowType.Shadow7;

if (shape.ShadowFormat.Type == ShadowType.ShadowMixed)
    shape.ShadowFormat.Clear();
```

### أنظر أيضا

* class [ShadowFormat](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
