---
title: ShadowFormat.Visible
linktitle: Visible
articleTitle: Visible
second_title: Aspose.Words لـ .NET
description: ShadowFormat Visible ملكية. إرجاعحقيقي إذا كان التنسيق المطبق على هذا المثيل مرئيًا في C#.
type: docs
weight: 20
url: /ar/net/aspose.words.drawing/shadowformat/visible/
---
## ShadowFormat.Visible property

إرجاع`حقيقي` إذا كان التنسيق المطبق على هذا المثيل مرئيًا.

```csharp
public bool Visible { get; }
```

## ملاحظات

على عكس[`Clear`](../clear/) ، إسناد`خطأ شنيع` إلى مرئي لا يمسح التنسيق، فهو يخفي تأثير الشكل فقط.

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
