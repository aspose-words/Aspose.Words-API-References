---
title: CheckBoxControl Class
linktitle: CheckBoxControl
articleTitle: CheckBoxControl
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Drawing.Ole.CheckBoxControl لتبديل قيم مربع الاختيار بسهولة وتعزيز أتمتة المستندات لديك من خلال التكامل السلس.
type: docs
weight: 1440
url: /ar/net/aspose.words.drawing.ole/checkboxcontrol/
---
## CheckBoxControl class

يقوم عنصر التحكم CheckBox بتبديل القيمة.

```csharp
public class CheckBoxControl : MorphDataControl
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [BackColor](../../aspose.words.drawing.ole/forms2olecontrol/backcolor/) { get; set; } | يحصل على لون الخلفية لعنصر التحكم أو يعينه. تعتمد القيمة الافتراضية على نوع عنصر التحكم. |
| [Caption](../../aspose.words.drawing.ole/forms2olecontrol/caption/) { get; set; } | يحصل على خاصية Caption الخاصة بالعنصر التحكم أو يعينها. القيمة الافتراضية هي سلسلة فارغة. |
| [Checked](../../aspose.words.drawing.ole/checkboxcontrol/checked/) { get; set; } | يحصل على قيمة منطقية تشير إلى هذا أو يعينها`CheckBoxControl` تم تحديده أم لا. القيمة الافتراضية هي`خطأ شنيع` . |
| virtual [ChildNodes](../../aspose.words.drawing.ole/forms2olecontrol/childnodes/) { get; } | يحصل على مجموعة من عناصر التحكم الفرعية الفورية. |
| [Enabled](../../aspose.words.drawing.ole/forms2olecontrol/enabled/) { get; } | إرجاع`حقيقي` إذا كان التحكم في حالة تمكين. |
| [ForeColor](../../aspose.words.drawing.ole/forms2olecontrol/forecolor/) { get; set; } | يحصل على لون المقدمة لعنصر التحكم أو يعينه. تعتمد القيمة الافتراضية على نوع عنصر التحكم. |
| [GroupName](../../aspose.words.drawing.ole/forms2olecontrol/groupname/) { get; set; } | يحصل على سلسلة تحدد مجموعة من عناصر التحكم المتبادلة الحصرية أو يعينها. القيمة الافتراضية هي سلسلة فارغة. |
| [Height](../../aspose.words.drawing.ole/forms2olecontrol/height/) { get; set; } | يحصل على ارتفاع عنصر التحكم بالنقاط أو يعينه. |
| [IsForms2OleControl](../../aspose.words.drawing.ole/olecontrol/isforms2olecontrol/) { get; } | إرجاع`حقيقي` إذا كان التحكم هو[`Forms2OleControl`](../forms2olecontrol/) . |
| [Name](../../aspose.words.drawing.ole/olecontrol/name/) { get; set; } | يحصل على اسم عنصر التحكم ActiveX أو يعينه. |
| override [Type](../../aspose.words.drawing.ole/checkboxcontrol/type/) { get; } | يحصل على نوع عنصر التحكم في النماذج 2.0. |
| [Value](../../aspose.words.drawing.ole/forms2olecontrol/value/) { get; } | يحصل على خاصية القيمة الأساسية التي تمثل غالبًا حالة التحكم. على سبيل المثال، يحتوي زر الخيار المحدد على القيمة '1' بينما يحتوي زر الخيار غير المحدد على القيمة '0'. القيمة الافتراضية هي سلسلة فارغة. |
| [Width](../../aspose.words.drawing.ole/forms2olecontrol/width/) { get; set; } | يحصل على عرض عنصر التحكم بالنقاط أو يعينه. |

## ملاحظات

لديه ثلاث حالات محتملة: محدد، تم مسحه، وغير محدد ولا تم مسحه، يعني مزيجًا من حالات التشغيل والإيقاف.

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

* class [MorphDataControl](../morphdatacontrol/)
* مساحة الاسم [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* المجسم [Aspose.Words](../../)
