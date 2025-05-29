---
title: TextBoxControl.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية TextBoxControl Type لـ Forms 2.0، مما يتيح تخصيص عناصر التحكم بشكل سلس وتحسين تجربة المستخدم في تطبيقاتك.
type: docs
weight: 20
url: /ar/net/aspose.words.drawing.ole/textboxcontrol/type/
---
## TextBoxControl.Type property

يحصل على نوع عنصر التحكم في النماذج 2.0.

```csharp
public override Forms2OleControlType Type { get; }
```

## أمثلة

يوضح كيفية تغيير نص عنصر التحكم TextBox OLE.

```csharp
Document doc = new Document(MyDir + "Textbox control.docm");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
TextBoxControl textBoxControl = (TextBoxControl)shape.OleFormat.OleControl;
Assert.AreEqual("Aspose.Words test", textBoxControl.Text);

textBoxControl.Text = "Updated text";
Assert.AreEqual("Updated text", textBoxControl.Text);
Assert.AreEqual(Forms2OleControlType.Textbox, textBoxControl.Type);
```

### أنظر أيضا

* enum [Forms2OleControlType](../../forms2olecontroltype/)
* class [TextBoxControl](../)
* مساحة الاسم [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* المجسم [Aspose.Words](../../../)
