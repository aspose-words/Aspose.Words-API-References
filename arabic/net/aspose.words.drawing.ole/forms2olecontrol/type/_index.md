---
title: Forms2OleControl.Type
second_title: Aspose.Words لمراجع .NET API
description: Forms2OleControl ملكية. الحصول على نوع التحكم في Forms 2.0.
type: docs
weight: 50
url: /ar/net/aspose.words.drawing.ole/forms2olecontrol/type/
---
## Forms2OleControl.Type property

الحصول على نوع التحكم في Forms 2.0.

```csharp
public abstract Forms2OleControlType Type { get; }
```

### أمثلة

يوضح كيفية التحقق من خصائص عنصر تحكم ActiveX.

```csharp
Document doc = new Document(MyDir + "ActiveX controls.docx");

Shape shape = (Shape) doc.GetChild(NodeType.Shape, 0, true);
OleControl oleControl = shape.OleFormat.OleControl;

Assert.AreEqual("CheckBox1", oleControl.Name);

if (oleControl.IsForms2OleControl)
{
    Forms2OleControl checkBox = (Forms2OleControl) oleControl;
    Assert.AreEqual("Первый", checkBox.Caption);
    Assert.AreEqual("0", checkBox.Value);
    Assert.AreEqual(true, checkBox.Enabled);
    Assert.AreEqual(Forms2OleControlType.CheckBox, checkBox.Type);
    Assert.AreEqual(null, checkBox.ChildNodes);
    Assert.AreEqual(string.Empty, checkBox.GroupName);

    // لاحظ أنه لا يمكنك تعيين اسم المجموعة للإطار.
    checkBox.GroupName = "Aspose group name";
}
```

### أنظر أيضا

* enum [Forms2OleControlType](../../forms2olecontroltype/)
* class [Forms2OleControl](../)
* مساحة الاسم [Aspose.Words.Drawing.Ole](../../forms2olecontrol/)
* المجسم [Aspose.Words](../../../)


