---
title: OptionButtonControl.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية نوع عنصر التحكم OptionButtonControl في Forms 2.0. تعلّم كيفية تحسين نماذجك باستخدام هذه الميزة الأساسية لنوع عنصر التحكم.
type: docs
weight: 20
url: /ar/net/aspose.words.drawing.ole/optionbuttoncontrol/type/
---
## OptionButtonControl.Type property

يحصل على نوع عنصر التحكم في النماذج 2.0.

```csharp
public override Forms2OleControlType Type { get; }
```

## أمثلة

يوضح كيفية تحديد زر الراديو.

```csharp
Document doc = new Document(MyDir + "Radio buttons.docx");

Shape shape1 = (Shape)doc.GetChild(NodeType.Shape, 0, true);
OptionButtonControl optionButton1 = (OptionButtonControl)shape1.OleFormat.OleControl;
// إلغاء تحديد العنصر المحدد الأول.
optionButton1.Selected = false;

Shape shape2 = (Shape)doc.GetChild(NodeType.Shape, 1, true);
OptionButtonControl optionButton2 = (OptionButtonControl)shape2.OleFormat.OleControl;
//اختر زر الخيار الثاني.
optionButton2.Selected = true;

Assert.AreEqual(Forms2OleControlType.OptionButton, optionButton1.Type);
Assert.AreEqual(Forms2OleControlType.OptionButton, optionButton2.Type);

doc.Save(ArtifactsDir + "Shape.SelectRadioControl.docx");
```

### أنظر أيضا

* enum [Forms2OleControlType](../../forms2olecontroltype/)
* class [OptionButtonControl](../)
* مساحة الاسم [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* المجسم [Aspose.Words](../../../)
