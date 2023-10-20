---
title: Forms2OleControl Class
linktitle: Forms2OleControl
articleTitle: Forms2OleControl
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Drawing.Ole.Forms2OleControl فصل. يمثل عنصر تحكم OLE لـ Microsoft Forms 2.0 في C#.
type: docs
weight: 1110
url: /ar/net/aspose.words.drawing.ole/forms2olecontrol/
---
## Forms2OleControl class

يمثل عنصر تحكم OLE لـ Microsoft Forms 2.0.

لمعرفة المزيد، قم بزيارة[العمل مع كائنات Ole](https://docs.aspose.com/words/net/working-with-ole-objects/) مقالة توثيقية.

```csharp
public abstract class Forms2OleControl : OleControl
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Caption](../../aspose.words.drawing.ole/forms2olecontrol/caption/) { get; } | يحصل على خاصية التسمية التوضيحية للتحكم. القيمة الافتراضية هي سلسلة فارغة. |
| virtual [ChildNodes](../../aspose.words.drawing.ole/forms2olecontrol/childnodes/) { get; } | يحصل على مجموعة من عناصر التحكم التابعة المباشرة. |
| [Enabled](../../aspose.words.drawing.ole/forms2olecontrol/enabled/) { get; } | إرجاع`حقيقي` إذا كان التحكم في حالة التمكين. |
| [GroupName](../../aspose.words.drawing.ole/forms2olecontrol/groupname/) { get; set; } | الحصول على أو تعيين سلسلة تحدد مجموعة من عناصر التحكم المتبادلة. القيمة الافتراضية هي سلسلة فارغة. |
| [IsForms2OleControl](../../aspose.words.drawing.ole/olecontrol/isforms2olecontrol/) { get; } | إرجاع`حقيقي` إذا كان التحكم أ`Forms2OleControl` . |
| [Name](../../aspose.words.drawing.ole/olecontrol/name/) { get; set; } | الحصول على اسم عنصر تحكم ActiveX أو تعيينه. |
| abstract [Type](../../aspose.words.drawing.ole/forms2olecontrol/type/) { get; } | الحصول على نوع التحكم في Forms 2.0. |
| [Value](../../aspose.words.drawing.ole/forms2olecontrol/value/) { get; } | يحصل على خاصية القيمة الأساسية التي غالبًا ما تمثل حالة التحكم. على سبيل المثال، يحتوي زر الخيار المحدد على القيمة "1" بينما يحتوي زر الخيار غير المحدد على "0". القيمة الافتراضية هي سلسلة فارغة. |

## أمثلة

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

* class [OleControl](../olecontrol/)
* مساحة الاسم [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* المجسم [Aspose.Words](../../)
