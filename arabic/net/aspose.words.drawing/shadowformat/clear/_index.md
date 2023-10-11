---
title: ShadowFormat.Clear
second_title: Aspose.Words لمراجع .NET API
description: ShadowFormat طريقة. مسح تنسيق الظل.
type: docs
weight: 30
url: /ar/net/aspose.words.drawing/shadowformat/clear/
---
## ShadowFormat.Clear method

مسح تنسيق الظل.

```csharp
public void Clear()
```

### أمثلة

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
* مساحة الاسم [Aspose.Words.Drawing](../../shadowformat/)
* المجسم [Aspose.Words](../../../)


