---
title: CheckBoxControl.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية CheckBoxControl Type لـ Forms 2.0، والتي تتيح لك فتح خيارات التحكم المتنوعة لتحسين وظائف تطبيقك.
type: docs
weight: 20
url: /ar/net/aspose.words.drawing.ole/checkboxcontrol/type/
---
## CheckBoxControl.Type property

يحصل على نوع عنصر التحكم في النماذج 2.0.

```csharp
public override Forms2OleControlType Type { get; }
```

## أمثلة

يوضح كيفية تغيير حالة عنصر التحكم CheckBox.

```csharp
Document doc = new Document(MyDir + "ActiveX controls.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
CheckBoxControl checkBoxControl = (CheckBoxControl)shape.OleFormat.OleControl;
checkBoxControl.Checked = true;

Assert.AreEqual(true, checkBoxControl.Checked);
Assert.AreEqual(Forms2OleControlType.CheckBox, checkBoxControl.Type);
```

### أنظر أيضا

* enum [Forms2OleControlType](../../forms2olecontroltype/)
* class [CheckBoxControl](../)
* مساحة الاسم [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* المجسم [Aspose.Words](../../../)
