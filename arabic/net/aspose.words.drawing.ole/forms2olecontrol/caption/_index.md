---
title: Forms2OleControl.Caption
linktitle: Caption
articleTitle: Caption
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية التسمية التوضيحية في Forms2OleControl لتخصيص عنوان عنصر التحكم بسهولة. حسّن تجربة المستخدم بهذه الميزة البسيطة والفعّالة.
type: docs
weight: 20
url: /ar/net/aspose.words.drawing.ole/forms2olecontrol/caption/
---
## Forms2OleControl.Caption property

يحصل على خاصية Caption الخاصة بالعنصر التحكم أو يعينها. القيمة الافتراضية هي سلسلة فارغة.

```csharp
public string Caption { get; set; }
```

## أمثلة

يوضح كيفية تعيين التسمية التوضيحية لعنصر التحكم ActiveX.

```csharp
DocumentBuilder builder = new DocumentBuilder();

CommandButtonControl button1 = new CommandButtonControl() { Caption = "Button caption" };
Shape shape = builder.InsertForms2OleControl(button1);
Assert.AreEqual("Button caption", button1.Caption);
```

يوضح كيفية التحقق من خصائص عنصر التحكم ActiveX.

```csharp
Document doc = new Document(MyDir + "ActiveX controls.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
OleControl oleControl = shape.OleFormat.OleControl;

Assert.AreEqual("CheckBox1", oleControl.Name);

if (oleControl.IsForms2OleControl)
{
    Forms2OleControl checkBox = (Forms2OleControl)oleControl;
    Assert.AreEqual("First", checkBox.Caption);
    Assert.AreEqual("0", checkBox.Value);
    Assert.AreEqual(true, checkBox.Enabled);
    Assert.AreEqual(Forms2OleControlType.CheckBox, checkBox.Type);
    Assert.AreEqual(null, checkBox.ChildNodes);
    Assert.AreEqual(string.Empty, checkBox.GroupName);

    // لاحظ أنه لا يمكنك تعيين GroupName لإطار.
    checkBox.GroupName = "Aspose group name";
}
```

### أنظر أيضا

* class [Forms2OleControl](../)
* مساحة الاسم [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* المجسم [Aspose.Words](../../../)
