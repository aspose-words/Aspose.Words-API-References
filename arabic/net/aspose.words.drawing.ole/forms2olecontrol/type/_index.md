---
title: Forms2OleControl.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Type في Forms2OleControl لاسترداد نوع عناصر التحكم في Forms 2.0 بسهولة، مما يعزز وظائف تطبيقك وكفاءته.
type: docs
weight: 80
url: /ar/net/aspose.words.drawing.ole/forms2olecontrol/type/
---
## Forms2OleControl.Type property

يحصل على نوع عنصر التحكم في النماذج 2.0.

```csharp
public abstract Forms2OleControlType Type { get; }
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

* enum [Forms2OleControlType](../../forms2olecontroltype/)
* class [Forms2OleControl](../)
* مساحة الاسم [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* المجسم [Aspose.Words](../../../)
