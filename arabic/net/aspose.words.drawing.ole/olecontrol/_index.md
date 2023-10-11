---
title: Class OleControl
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Drawing.Ole.OleControl فصل. يمثل عنصر تحكم OLE ActiveX.
type: docs
weight: 1140
url: /ar/net/aspose.words.drawing.ole/olecontrol/
---
## OleControl class

يمثل عنصر تحكم OLE ActiveX.

لمعرفة المزيد، قم بزيارة[العمل مع كائنات Ole](https://docs.aspose.com/words/net/working-with-ole-objects/) مقالة توثيقية.

```csharp
public class OleControl
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [IsForms2OleControl](../../aspose.words.drawing.ole/olecontrol/isforms2olecontrol/) { get; } | إرجاع`حقيقي` إذا كان التحكم أ[`Forms2OleControl`](../forms2olecontrol/) . |
| [Name](../../aspose.words.drawing.ole/olecontrol/name/) { get; set; } | الحصول على اسم عنصر تحكم ActiveX أو تعيينه. |

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

* مساحة الاسم [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* المجسم [Aspose.Words](../../)


