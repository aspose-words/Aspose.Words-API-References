---
title: OleFormat.OleControl
second_title: Aspose.Words لمراجع .NET API
description: OleFormat ملكية. يحصلOleControl الكائنات إذا كان كائن OLE هذا هو عنصر تحكم ActiveX. وإلا فإن هذه الخاصية فارغة.
type: docs
weight: 60
url: /ar/net/aspose.words.drawing/oleformat/olecontrol/
---
## OleFormat.OleControl property

يحصل`OleControl` الكائنات إذا كان كائن OLE هذا هو عنصر تحكم ActiveX. وإلا فإن هذه الخاصية فارغة.

```csharp
public OleControl OleControl { get; }
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

* class [OleControl](../../../aspose.words.drawing.ole/olecontrol/)
* class [OleFormat](../)
* مساحة الاسم [Aspose.Words.Drawing](../../oleformat/)
* المجسم [Aspose.Words](../../../)


