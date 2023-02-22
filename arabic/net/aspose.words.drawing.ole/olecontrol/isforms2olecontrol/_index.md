---
title: OleControl.IsForms2OleControl
second_title: Aspose.Words لمراجع .NET API
description: OleControl ملكية. إرجاع صحيح إذا كان عنصر التحكمForms2OleControl .
type: docs
weight: 10
url: /ar/net/aspose.words.drawing.ole/olecontrol/isforms2olecontrol/
---
## OleControl.IsForms2OleControl property

إرجاع صحيح إذا كان عنصر التحكم[`Forms2OleControl`](../../forms2olecontrol/) .

```csharp
public virtual bool IsForms2OleControl { get; }
```

### أمثلة

يوضح كيفية التحقق من خصائص عنصر تحكم ActiveX.

```csharp
Document doc = new Document(MyDir + "ActiveX controls.docx");

Shape shape = (Shape) doc.GetChild(NodeType.Shape, 0, true);
OleControl oleControl = shape.OleFormat.OleControl;

Assert.AreEqual(null, oleControl.Name);

if (oleControl.IsForms2OleControl)
{
    Forms2OleControl checkBox = (Forms2OleControl) oleControl;
    Assert.AreEqual("Первый", checkBox.Caption);
    Assert.AreEqual("0", checkBox.Value);
    Assert.AreEqual(true, checkBox.Enabled);
    Assert.AreEqual(Forms2OleControlType.CheckBox, checkBox.Type);
    Assert.AreEqual(null, checkBox.ChildNodes);
}
```

### أنظر أيضا

* class [OleControl](../)
* مساحة الاسم [Aspose.Words.Drawing.Ole](../../olecontrol/)
* المجسم [Aspose.Words](../../../)


