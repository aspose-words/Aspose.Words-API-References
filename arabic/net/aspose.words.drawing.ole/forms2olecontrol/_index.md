---
title: Class Forms2OleControl
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Drawing.Ole.Forms2OleControl فصل. يمثل عنصر تحكم Microsoft Forms 2.0 OLE.
type: docs
weight: 980
url: /ar/net/aspose.words.drawing.ole/forms2olecontrol/
---
## Forms2OleControl class

يمثل عنصر تحكم Microsoft Forms 2.0 OLE.

```csharp
public abstract class Forms2OleControl : OleControl
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Caption](../../aspose.words.drawing.ole/forms2olecontrol/caption/) { get; } | يحصل على خاصية التسمية التوضيحية للتحكم. القيمة الافتراضية هي سلسلة فارغة. |
| [ChildNodes](../../aspose.words.drawing.ole/forms2olecontrol/childnodes/) { get; } | الحصول على مجموعة من عناصر التحكم الفوري للأطفال. |
| [Enabled](../../aspose.words.drawing.ole/forms2olecontrol/enabled/) { get; } | إرجاع صحيح إذا كان التحكم في حالة تمكين. |
| override [IsForms2OleControl](../../aspose.words.drawing.ole/forms2olecontrol/isforms2olecontrol/) { get; } |  |
| [Name](../../aspose.words.drawing.ole/olecontrol/name/) { get; } | الحصول على اسم عنصر تحكم ActiveX . |
| [Type](../../aspose.words.drawing.ole/forms2olecontrol/type/) { get; } | الحصول على عنصر تحكم 2.0 من النماذج . |
| [Value](../../aspose.words.drawing.ole/forms2olecontrol/value/) { get; } | يحصل على خاصية القيمة الأساسية التي غالبًا ما تمثل حالة التحكم . على سبيل المثال ، يحتوي زر الخيار المحدد على قيمة "1" بينما لم يتم تحديده يحتوي على "0" . القيمة الافتراضية هي سلسلة فارغة . |

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

* class [OleControl](../olecontrol/)
* مساحة الاسم [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* المجسم [Aspose.Words](../../)


