---
title: OleControl.Name
second_title: Aspose.Words لمراجع .NET API
description: OleControl ملكية. الحصول على اسم عنصر تحكم ActiveX أو تعيينه.
type: docs
weight: 20
url: /ar/net/aspose.words.drawing.ole/olecontrol/name/
---
## OleControl.Name property

الحصول على اسم عنصر تحكم ActiveX أو تعيينه.

```csharp
public string Name { get; set; }
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

* class [OleControl](../)
* مساحة الاسم [Aspose.Words.Drawing.Ole](../../olecontrol/)
* المجسم [Aspose.Words](../../../)


