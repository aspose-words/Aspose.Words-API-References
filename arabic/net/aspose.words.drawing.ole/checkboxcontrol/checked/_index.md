---
title: CheckBoxControl.Checked
linktitle: Checked
articleTitle: Checked
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية CheckBoxControl Checked، وأدر حالات مربعات الاختيار بسهولة باستخدام قيمة منطقية بسيطة. القيمة الافتراضية هي False للتحكم الأمثل.
type: docs
weight: 10
url: /ar/net/aspose.words.drawing.ole/checkboxcontrol/checked/
---
## CheckBoxControl.Checked property

يحصل على قيمة منطقية تشير إلى هذا أو يعينها[`CheckBoxControl`](../) تم تحديده أم لا. القيمة الافتراضية هي`خطأ شنيع` .

```csharp
public bool Checked { get; set; }
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

* class [CheckBoxControl](../)
* مساحة الاسم [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* المجسم [Aspose.Words](../../../)
