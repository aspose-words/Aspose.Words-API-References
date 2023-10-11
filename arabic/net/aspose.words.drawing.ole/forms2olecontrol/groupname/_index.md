---
title: Forms2OleControl.GroupName
second_title: Aspose.Words لمراجع .NET API
description: Forms2OleControl ملكية. الحصول على أو تعيين سلسلة تحدد مجموعة من عناصر التحكم المتبادلة. القيمة الافتراضية هي سلسلة فارغة.
type: docs
weight: 40
url: /ar/net/aspose.words.drawing.ole/forms2olecontrol/groupname/
---
## Forms2OleControl.GroupName property

الحصول على أو تعيين سلسلة تحدد مجموعة من عناصر التحكم المتبادلة. القيمة الافتراضية هي سلسلة فارغة.

```csharp
public string GroupName { get; set; }
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

* class [Forms2OleControl](../)
* مساحة الاسم [Aspose.Words.Drawing.Ole](../../forms2olecontrol/)
* المجسم [Aspose.Words](../../../)


