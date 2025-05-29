---
title: Forms2OleControl.Height
linktitle: Height
articleTitle: Height
second_title: Aspose.Words لـ .NET
description: اضبط ارتفاع Forms2OleControl بسهولة بالنقاط لعرض ووظائف مثالية. حسّن واجهة المستخدم لديك بأبعاد تحكم دقيقة!
type: docs
weight: 70
url: /ar/net/aspose.words.drawing.ole/forms2olecontrol/height/
---
## Forms2OleControl.Height property

يحصل على ارتفاع عنصر التحكم بالنقاط أو يعينه.

```csharp
public double Height { get; set; }
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
