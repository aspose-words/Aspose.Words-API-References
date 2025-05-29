---
title: TextBoxControl.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words لـ .NET
description: يمكنك إدارة نص TextBoxControl بسهولة - احصل على المحتوى الخاص به أو قم بتعيينه لتحقيق تفاعل سلس للمستخدم وتحسين الوظائف في تطبيقك.
type: docs
weight: 10
url: /ar/net/aspose.words.drawing.ole/textboxcontrol/text/
---
## TextBoxControl.Text property

يحصل على نص عنصر التحكم أو يعينه.

```csharp
public string Text { get; set; }
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

* class [TextBoxControl](../)
* مساحة الاسم [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* المجسم [Aspose.Words](../../../)
