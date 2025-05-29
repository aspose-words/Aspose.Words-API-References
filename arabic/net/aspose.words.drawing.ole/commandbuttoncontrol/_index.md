---
title: CommandButtonControl Class
linktitle: CommandButtonControl
articleTitle: CommandButtonControl
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Drawing.Ole.CommandButtonControl لإنشاء أزرار تفاعلية بسهولة لتشغيل وحدات الماكرو، مما يعزز مشاركة المستخدم في تطبيقاتك.
type: docs
weight: 1450
url: /ar/net/aspose.words.drawing.ole/commandbuttoncontrol/
---
## CommandButtonControl class

يقوم عنصر التحكم CommandButton بتشغيل ماكرو يقوم بتنفيذ إجراء عندما ينقر عليه المستخدم.

```csharp
public class CommandButtonControl : Forms2OleControl
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [CommandButtonControl](commandbuttoncontrol/)() | يقوم بتهيئة مثيل جديد لـ`CommandButtonControl` الصف. |

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
| override [Type](../../aspose.words.drawing.ole/commandbuttoncontrol/type/) { get; } | يحصل على نوع عنصر التحكم في النماذج 2.0. |
| [Value](../../aspose.words.drawing.ole/forms2olecontrol/value/) { get; } | يحصل على خاصية القيمة الأساسية التي تمثل غالبًا حالة التحكم. على سبيل المثال، يحتوي زر الخيار المحدد على القيمة '1' بينما يحتوي زر الخيار غير المحدد على القيمة '0'. القيمة الافتراضية هي سلسلة فارغة. |
| [Width](../../aspose.words.drawing.ole/forms2olecontrol/width/) { get; set; } | يحصل على عرض عنصر التحكم بالنقاط أو يعينه. |

## أمثلة

يوضح كيفية إدراج عنصر التحكم ActiveX.

```csharp
DocumentBuilder builder = new DocumentBuilder();

CommandButtonControl button1 = new CommandButtonControl();
Shape shape = builder.InsertForms2OleControl(button1);
Assert.AreEqual(Forms2OleControlType.CommandButton, button1.Type);
```

### أنظر أيضا

* class [Forms2OleControl](../forms2olecontrol/)
* مساحة الاسم [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* المجسم [Aspose.Words](../../)
