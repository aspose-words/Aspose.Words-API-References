---
title: OptionButtonControl Class
linktitle: OptionButtonControl
articleTitle: OptionButtonControl
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Drawing.Ole.OptionButtonControl، المثالية لإنشاء خيارات اختيار حصرية في تطبيقاتك. حسّن تجربة المستخدم اليوم!
type: docs
weight: 1510
url: /ar/net/aspose.words.drawing.ole/optionbuttoncontrol/
---
## OptionButtonControl class

يتيح عنصر التحكم OptionButton خيارًا واحدًا ضمن مجموعة محدودة من الخيارات المتبادلة الحصرية.

```csharp
public class OptionButtonControl : MorphDataControl
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [BackColor](../../aspose.words.drawing.ole/forms2olecontrol/backcolor/) { get; set; } | يحصل على لون الخلفية لعنصر التحكم أو يعينه. تعتمد القيمة الافتراضية على نوع عنصر التحكم. |
| [Caption](../../aspose.words.drawing.ole/forms2olecontrol/caption/) { get; set; } | يحصل على خاصية Caption الخاصة بالعنصر التحكم أو يعينها. القيمة الافتراضية هي سلسلة فارغة. |
| virtual [ChildNodes](../../aspose.words.drawing.ole/forms2olecontrol/childnodes/) { get; } | يحصل على مجموعة من عناصر التحكم الفرعية الفورية. |
| [Enabled](../../aspose.words.drawing.ole/forms2olecontrol/enabled/) { get; } | إرجاع`حقيقي` إذا كان التحكم في حالة تمكين. |
| [ForeColor](../../aspose.words.drawing.ole/forms2olecontrol/forecolor/) { get; set; } | يحصل على لون المقدمة لعنصر التحكم أو يعينه. تعتمد القيمة الافتراضية على نوع عنصر التحكم. |
| [GroupName](../../aspose.words.drawing.ole/forms2olecontrol/groupname/) { get; set; } | يحصل على سلسلة تحدد مجموعة من عناصر التحكم المتبادلة الحصرية أو يعينها. القيمة الافتراضية هي سلسلة فارغة. |
| [Height](../../aspose.words.drawing.ole/forms2olecontrol/height/) { get; set; } | يحصل على ارتفاع عنصر التحكم بالنقاط أو يعينه. |
| [IsForms2OleControl](../../aspose.words.drawing.ole/olecontrol/isforms2olecontrol/) { get; } | إرجاع`حقيقي` إذا كان التحكم هو[`Forms2OleControl`](../forms2olecontrol/) . |
| [Name](../../aspose.words.drawing.ole/olecontrol/name/) { get; set; } | يحصل على اسم عنصر التحكم ActiveX أو يعينه. |
| [Selected](../../aspose.words.drawing.ole/optionbuttoncontrol/selected/) { get; set; } | يحصل على قيمة منطقية تشير إلى هذا أو يعينها`OptionButtonControl` هل تم تحديده أم لا. |
| override [Type](../../aspose.words.drawing.ole/optionbuttoncontrol/type/) { get; } | يحصل على نوع عنصر التحكم في النماذج 2.0. |
| [Value](../../aspose.words.drawing.ole/forms2olecontrol/value/) { get; } | يحصل على خاصية القيمة الأساسية التي تمثل غالبًا حالة التحكم. على سبيل المثال، يحتوي زر الخيار المحدد على القيمة '1' بينما يحتوي زر الخيار غير المحدد على القيمة '0'. القيمة الافتراضية هي سلسلة فارغة. |
| [Width](../../aspose.words.drawing.ole/forms2olecontrol/width/) { get; set; } | يحصل على عرض عنصر التحكم بالنقاط أو يعينه. |

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

* class [MorphDataControl](../morphdatacontrol/)
* مساحة الاسم [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* المجسم [Aspose.Words](../../)
