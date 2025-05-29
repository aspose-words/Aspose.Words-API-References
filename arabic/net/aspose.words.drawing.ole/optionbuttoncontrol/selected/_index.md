---
title: OptionButtonControl.Selected
linktitle: Selected
articleTitle: Selected
second_title: Aspose.Words لـ .NET
description: أدر زرّ الخيار بكل سهولة! عيّن أو احصل على حالته المحددة بقيمة منطقية بسيطة لتفاعل سلس مع المستخدم.
type: docs
weight: 10
url: /ar/net/aspose.words.drawing.ole/optionbuttoncontrol/selected/
---
## OptionButtonControl.Selected property

يحصل على قيمة منطقية تشير إلى هذا أو يعينها[`OptionButtonControl`](../) هل تم تحديده أم لا.

```csharp
public bool Selected { get; set; }
```

## ملاحظات

ملاحظة، تسمح لك هذه الخاصية بتحديد عناصر متعددة في مجموعة من[`OptionButtonControl`](../) بنفس الشيء[`GroupName`](../../forms2olecontrol/groupname/) . يقع على عاتقك مسؤولية الاهتمام بإلغاء تحديد عنصر تم تحديده مسبقًا عند إجراء هذا[`OptionButtonControl`](../) تم التحديد.

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

* class [OptionButtonControl](../)
* مساحة الاسم [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* المجسم [Aspose.Words](../../../)
