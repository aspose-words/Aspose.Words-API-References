---
title: Forms2OleControl.ForeColor
linktitle: ForeColor
articleTitle: ForeColor
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ForeColor في Forms2OleControl لتخصيص لون مقدمة عنصر التحكم بسهولة. حسّن واجهة المستخدم الخاصة بك بخيارات ألوان مخصصة اليوم!
type: docs
weight: 50
url: /ar/net/aspose.words.drawing.ole/forms2olecontrol/forecolor/
---
## Forms2OleControl.ForeColor property

يحصل على لون المقدمة لعنصر التحكم أو يعينه. تعتمد القيمة الافتراضية على نوع عنصر التحكم.

```csharp
public Color ForeColor { get; set; }
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
