---
title: TextBoxControl Class
linktitle: TextBoxControl
articleTitle: TextBoxControl
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Drawing.Ole.TextBoxControl لعرض نص منظم بسهولة من البيانات أو مدخلات المستخدم. حسّن إدارة مستنداتك اليوم!
type: docs
weight: 1520
url: /ar/net/aspose.words.drawing.ole/textboxcontrol/
---
## TextBoxControl class

يعرض عنصر التحكم TextBox نصًا من مجموعة منظمة من البيانات أو إدخال المستخدم.

```csharp
public class TextBoxControl : MorphDataControl
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
| [Text](../../aspose.words.drawing.ole/textboxcontrol/text/) { get; set; } | يحصل على نص عنصر التحكم أو يعينه. |
| override [Type](../../aspose.words.drawing.ole/textboxcontrol/type/) { get; } | يحصل على نوع عنصر التحكم في النماذج 2.0. |
| [Value](../../aspose.words.drawing.ole/forms2olecontrol/value/) { get; } | يحصل على خاصية القيمة الأساسية التي تمثل غالبًا حالة التحكم. على سبيل المثال، يحتوي زر الخيار المحدد على القيمة '1' بينما يحتوي زر الخيار غير المحدد على القيمة '0'. القيمة الافتراضية هي سلسلة فارغة. |
| [Width](../../aspose.words.drawing.ole/forms2olecontrol/width/) { get; set; } | يحصل على عرض عنصر التحكم بالنقاط أو يعينه. |

## أمثلة

يوضح كيفية تغيير نص عنصر التحكم TextBox OLE.

```csharp
Document doc = new Document(MyDir + "Textbox control.docm");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
TextBoxControl textBoxControl = (TextBoxControl)shape.OleFormat.OleControl;
Assert.AreEqual("Aspose.Words test", textBoxControl.Text);

textBoxControl.Text = "Updated text";
Assert.AreEqual("Updated text", textBoxControl.Text);
Assert.AreEqual(Forms2OleControlType.Textbox, textBoxControl.Type);
```

### أنظر أيضا

* class [MorphDataControl](../morphdatacontrol/)
* مساحة الاسم [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* المجسم [Aspose.Words](../../)
