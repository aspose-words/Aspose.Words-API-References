---
title: Forms2OleControl.Width
linktitle: Width
articleTitle: Width
second_title: Aspose.Words لـ .NET
description: اكتشف كيفية تعديل خاصية العرض في Forms2OleControl بسهولة للتحكم الدقيق في حجم النقاط. حسّن تصميم واجهة المستخدم لديك بسهولة!
type: docs
weight: 100
url: /ar/net/aspose.words.drawing.ole/forms2olecontrol/width/
---
## Forms2OleControl.Width property

يحصل على عرض عنصر التحكم بالنقاط أو يعينه.

```csharp
public double Width { get; set; }
```

## أمثلة

يوضح كيفية تعيين خصائص عنصر التحكم ActiveX.

```csharp
Document doc = new Document(MyDir + "ActiveX controls.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Forms2OleControl oleControl = (Forms2OleControl)shape.OleFormat.OleControl;
oleControl.ForeColor = Color.FromArgb(0x17, 0xE1, 0x35);
oleControl.BackColor = Color.FromArgb(0x33, 0x97, 0xF4);
oleControl.Height = 100.54;
oleControl.Width = 201.06;
```

### أنظر أيضا

* class [Forms2OleControl](../)
* مساحة الاسم [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* المجسم [Aspose.Words](../../../)
