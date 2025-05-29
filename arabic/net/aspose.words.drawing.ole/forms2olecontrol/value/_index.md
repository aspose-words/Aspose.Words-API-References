---
title: Forms2OleControl.Value
linktitle: Value
articleTitle: Value
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية قيمة Forms2OleControl، التي تعكس حالات التحكم. أدر قيم أزرار الخيارات بسهولة، 1 للخيار المحدد، و0 للخيار غير المحدد. بسّط برمجة جهازك!
type: docs
weight: 90
url: /ar/net/aspose.words.drawing.ole/forms2olecontrol/value/
---
## Forms2OleControl.Value property

يحصل على خاصية القيمة الأساسية التي تمثل غالبًا حالة التحكم. على سبيل المثال، يحتوي زر الخيار المحدد على القيمة '1' بينما يحتوي زر الخيار غير المحدد على القيمة '0'. القيمة الافتراضية هي سلسلة فارغة.

```csharp
public string Value { get; }
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

* class [Forms2OleControl](../)
* مساحة الاسم [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* المجسم [Aspose.Words](../../../)
