---
title: OleControl.Name
linktitle: Name
articleTitle: Name
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية اسم OleControl لإدارة اسم عنصر تحكم ActiveX بسهولة. حسّن وظائفك وسهّل عملية التطوير لديك اليوم!
type: docs
weight: 20
url: /ar/net/aspose.words.drawing.ole/olecontrol/name/
---
## OleControl.Name property

يحصل على اسم عنصر التحكم ActiveX أو يعينه.

```csharp
public string Name { get; set; }
```

## أمثلة

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

* class [OleControl](../)
* مساحة الاسم [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* المجسم [Aspose.Words](../../../)
