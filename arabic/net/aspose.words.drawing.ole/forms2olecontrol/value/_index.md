---
title: Forms2OleControl.Value
second_title: Aspose.Words لمراجع .NET API
description: Forms2OleControl ملكية. يحصل على خاصية القيمة الأساسية التي غالبًا ما تمثل حالة التحكم . على سبيل المثال  يحتوي زر الخيار المحدد على قيمة 1 بينما لم يتم تحديده يحتوي على 0 . القيمة الافتراضية هي سلسلة فارغة .
type: docs
weight: 60
url: /ar/net/aspose.words.drawing.ole/forms2olecontrol/value/
---
## Forms2OleControl.Value property

يحصل على خاصية القيمة الأساسية التي غالبًا ما تمثل حالة التحكم . على سبيل المثال ، يحتوي زر الخيار المحدد على قيمة "1" بينما لم يتم تحديده يحتوي على "0" . القيمة الافتراضية هي سلسلة فارغة .

```csharp
public string Value { get; }
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

* class [Forms2OleControl](../)
* مساحة الاسم [Aspose.Words.Drawing.Ole](../../forms2olecontrol/)
* المجسم [Aspose.Words](../../../)


